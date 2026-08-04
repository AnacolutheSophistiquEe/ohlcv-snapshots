# MSTR

**Generated** : 2026-08-04T21:58:46.025157+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $97.65  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $97.65 (+2.0% vs entrée) · entrée $95.74 · stop $91.91 · T1 $97.72 · R/R 0.52  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk -0.073 _(réel 5 s)_ (GBM -0.009) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 1522 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $95.35–$96.14 (mid $95.74)
- Spot actuel : $97.65 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $91.91 (stop swing_plan-based (-10.23%))
- Targets : T1 $97.72 · R/R 0.52 | T2 $99.70 · R/R 1.03 | T3 $101.68 · R/R 1.55
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $91.91


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.034 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 25 % | T3 16 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.0 | bear 12.2 | side 18.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.958% → cible +2.068% / stop −4.0%, p_fill 56%, n_eff≈25.0) : P(cible|rempli) **45%** · **EV/risk -0.073** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −4.295% → cible +4.625% / stop −6.201%, p_fill 43%, n_eff≈20.6) : P(cible|rempli) **56%** · **EV/risk -0.021** (×p_fill ; si rempli -0.30% du capital)
  - **deep** (entrée dip −6.638% → cible +6.541% / stop −9.535%, p_fill 48%, n_eff≈22.0) : P(cible|rempli) **55%** · **EV/risk -0.008** (×p_fill ; si rempli -0.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→61% · +3.0%→42% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.59% (p90 9.85%) · excursion haute méd. +2.74% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.473% vs midi 1.234% vs clôture 1.367% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.101 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.118% ; recovery-V 34%
- **σ réalisé intraday** 3.89% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 58% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 95.3225 (VA 94.6975–95.5725 ; dernier close 94.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 55% (gap-down >1% 42% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.06%) · haut méd +0.75% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.17% (p90 −2.83%) · haut méd +1.14% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.48%) · haut méd +1.45% · range méd 3.22%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −4.23%) · haut méd +1.7% · range méd 3.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (126/159) · gap 48% · délai 0.0min · rebond 49% (62/126) (MFE +0.96%)
   - −1.0% : fill 30min 63% · séance 74% (120/159) · gap 42% · délai 0.0min · rebond 56% (69/120) (MFE +1.16%)
   - −1.5% : fill 30min 57% · séance 68% (111/159) · gap 33% · délai 0.0min · rebond 57% (64/111) (MFE +1.49%)
   - −2.0% : fill 30min 50% · séance 63% (101/159) · gap 27% · délai 0.0min · rebond 59% (63/101) (MFE +1.32%)
   - −3.0% : fill 30min 37% · séance 52% (77/159) · gap 17% · délai 1.2min · rebond 59% (47/77) (MFE +1.57%)
   - −4.0% : fill 30min 25% · séance 44% (64/159) · gap 6% · délai 12.7min · rebond 64% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 18% · séance 30% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.28%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −2.75%) → stop au-delà de −2.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.1% (p90 −2.71%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=954 jambes) : jambe baissière méd −1.14% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (76/77) · rebond 48% (38/76)
      · −2.0% : fill 93% (69/77) · rebond 58% (40/69)
      · −3.0% : fill 83% (60/77) · rebond 59% (36/60)
      · −4.0% : fill 70% (50/77) · rebond 67% (33/50)
      · −5.0% : fill 50% (38/77) · rebond 76% (28/38)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (76 cas) · 38% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 46% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **77%** · continue >prix actuel 56% ; creux résiduel méd -1.46% (q20 -2.73%) → **SL/trailing à −2.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.89% / q75 +3.15% → **scale +1.89% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **15%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.55% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.56% .. +3.8%] · haut q95 +4.08% · bas q05 -3.97%
   - 60min (n=160) : retour [-4.9% .. +3.51%] · haut q95 +5.25% · bas q05 -5.55%
   - 2h (n=160) : retour [-4.64% .. +5.52%] · haut q95 +5.85% · bas q05 -5.55%
   - 4h (n=160) : retour [-6.89% .. +6.79%] · haut q95 +8.52% · bas q05 -7.49%
   - 6h (n=160) : retour [-5.96% .. +6.29%] · haut q95 +8.52% · bas q05 -8.14%
   - session (n=160) : retour [-5.68% .. +6.02%] · haut q95 +8.52% · bas q05 -8.14%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 8% vs absente 2% (base 6%)
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
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 50.2  _(neutre)_
- **ADX** : 12.3  _(pas de tendance nette)_
- **MACD** : hist 1.384  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 11.4%
- **ATR** : 5.8 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.081  _(accumulation)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 63.0  _(marche en range (choppy))_
- **MA** : MA20 95.76 · MA50 109.92 · MA200 155.81  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -11.2% · MA200 -37.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89095 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
