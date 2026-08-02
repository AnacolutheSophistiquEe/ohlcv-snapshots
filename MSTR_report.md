# MSTR

**Generated** : 2026-08-02T14:55:53.572115+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $93.28  

> 🟡 **WAIT-FOR-DIP** — spot +0.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $93.28 (+0.9% vs entrée) · entrée $92.47 · stop $88.77 · T1 $94.37 · R/R 0.51  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM -0.008) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -335 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $92.08–$92.85 (mid $92.47)
- Spot actuel : $93.28 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $88.77 (stop swing_plan-based (-8.27%))
- Targets : T1 $94.37 · R/R 0.51 | T2 $96.27 · R/R 1.03 | T3 $98.18 · R/R 1.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $88.77


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.030 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 26 % | T3 16 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 75.1 | bear 10.7 | side 14.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 93.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.875% → cible +2.059% / stop −4.0%, p_fill 82%, n_eff≈36.1) : P(cible|rempli) **58%** · **EV/risk +0.009** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −1.919% → cible +4.605% / stop −6.476%, p_fill 70%, n_eff≈31.0) : P(cible|rempli) **47%** · **EV/risk -0.158** (×p_fill ; si rempli -1.47% du capital)
  - **deep** (entrée dip −2.974% → cible +6.512% / stop −9.818%, p_fill 80%, n_eff≈32.3) : P(cible|rempli) **64%** · **EV/risk +0.016** (×p_fill ; si rempli +0.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→61% · +3.0%→42% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.61% (p90 9.85%) · excursion haute méd. +2.74% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.459% vs midi 1.234% vs clôture 1.368% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; neutre — autocorr -0.011)_ ; drift intra méd. -0.27% ; recovery-V 34%
- **σ réalisé intraday** 3.903% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 61% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 93.6396 (VA 91.5991–94.9514 ; dernier close 93.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.29% · baisse 54% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.06%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −2.83%) · haut méd +1.1% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.48%) · haut méd +1.41% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.8% (p90 −4.28%) · haut méd +1.63% · range méd 3.87%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (126/159) · gap 47% · délai 0.0min · rebond 48% (61/126) (MFE +0.94%)
   - −1.0% : fill 30min 62% · séance 73% (120/159) · gap 41% · délai 0.0min · rebond 55% (68/120) (MFE +1.07%)
   - −1.5% : fill 30min 56% · séance 68% (111/159) · gap 34% · délai 0.0min · rebond 55% (63/111) (MFE +1.32%)
   - −2.0% : fill 30min 50% · séance 63% (101/159) · gap 28% · délai 0.0min · rebond 58% (63/101) (MFE +1.2%)
   - −3.0% : fill 30min 38% · séance 53% (78/159) · gap 17% · délai 1.2min · rebond 59% (47/78) (MFE +1.57%)
   - −4.0% : fill 30min 26% · séance 45% (65/159) · gap 6% · délai 12.8min · rebond 64% (40/65) (MFE +1.65%)
   - −5.0% : fill 30min 18% · séance 31% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −2.28%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.12% (p90 −2.76%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.16% (p90 −2.72%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=954 jambes) : jambe baissière méd −1.15% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 99% (76/77) · rebond 45% (37/76)
      · −2.0% : fill 93% (69/77) · rebond 56% (40/69)
      · −3.0% : fill 86% (61/77) · rebond 59% (36/61)
      · −4.0% : fill 73% (51/77) · rebond 67% (33/51)
      · −5.0% : fill 52% (38/77) · rebond 76% (28/38)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (15/16) · rebond 89% (11/15)
      · −2.0% : fill 65% (11/16) · rebond 48% (7/11)
      · −3.0% : fill 36% (6/16) · rebond 57% (4/6)
      · −4.0% : fill 23% (5/16) · rebond 13% (2/5)
      · −5.0% : fill 18% (4/16) · rebond 16% (2/4)
   - **gap-up** (66 séances) :
      · −1.0% : fill 35% (29/66) · rebond 66% (20/29)
      · −2.0% : fill 24% (21/66) · rebond 71% (16/21)
      · −3.0% : fill 16% (11/66) · rebond 56% (7/11)
      · −4.0% : fill 14% (9/66) · rebond 66% (5/9)
      · −5.0% : fill 7% (5/66) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 52% si les 15 1res min sont vertes (75 cas) · 38% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 45% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **76%** · continue >prix actuel 58% ; creux résiduel méd -1.51% (q20 -2.77%) → **SL/trailing à −2.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.95% / q75 +3.15% → **scale +1.95% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **15%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.54% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.59% .. +3.83%] · haut q95 +4.1% · bas q05 -3.97%
   - 60min (n=160) : retour [-4.9% .. +3.45%] · haut q95 +5.26% · bas q05 -5.57%
   - 2h (n=160) : retour [-4.65% .. +5.53%] · haut q95 +5.86% · bas q05 -5.57%
   - 4h (n=160) : retour [-6.95% .. +6.95%] · haut q95 +8.55% · bas q05 -8.04%
   - 6h (n=160) : retour [-6.03% .. +6.37%] · haut q95 +8.63% · bas q05 -8.17%
   - session (n=160) : retour [-5.71% .. +6.04%] · haut q95 +8.63% · bas q05 -8.17%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **17%**. Lecture précoce 30 min : signature présente → 8% vs absente 2% (base 6%)
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
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 51.2  _(neutre)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist 1.363  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 12.2%
- **ATR** : 5.92 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.018  _(neutre)_
- **Vol ratio** : 1.28  _(volume normal)_
- **Choppiness** : 63.8  _(marche en range (choppy))_
- **MA** : MA20 96.04 · MA50 112.68 · MA200 157.84  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 -17.2% · MA200 -40.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91332 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
