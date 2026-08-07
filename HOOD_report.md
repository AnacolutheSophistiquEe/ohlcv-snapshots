# HOOD

**Generated** : 2026-08-07T00:31:23.162247+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $90.71  

> 🟡 **WAIT-FOR-DIP** — spot +2.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $90.71 (+2.5% vs entrée) · entrée $88.50 · stop $85.84 · T1 $90.36 · R/R 0.7  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.09 _(réel 5 s)_ (GBM -0.012) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $88.13–$88.87 (mid $88.50)
- Spot actuel : $90.71 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $85.84 (stop swing_plan-based (-11.51%))
- Targets : T1 $90.36 · R/R 0.7 | T2 $92.23 · R/R 1.4 | T3 $94.09 · R/R 2.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $85.84


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : $-0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 24 % | T3 20 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.2 | bear 28.8 | side 65.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.433% → cible +2.105% / stop −3.0%, p_fill 57%, n_eff≈21.9) : P(cible|rempli) **59%** · **EV/risk +0.090** (×p_fill ; si rempli +0.47% du capital)
  - **swing** (entrée dip −5.357% → cible +4.707% / stop −6.501%, p_fill 40%, n_eff≈13.2) : P(cible|rempli) **56%** · **EV/risk -0.035** (×p_fill ; si rempli -0.56% du capital)
  - **deep** (entrée dip −8.28% → cible +6.656% / stop −10.063%, p_fill 38%, n_eff≈11.8) : P(cible|rempli) **33%** · **EV/risk -0.160** (×p_fill ; si rempli -4.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→55% · +3.0%→35% · +5.0%→20% · +8.0%→6%
- Range intraday médian 5.11% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.35%
- Profil de vol intra : ouverture 3.719% vs midi 1.051% vs clôture 1.137% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 72% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; momentum — autocorr 0.039)_ ; drift intra méd. -0.184% ; recovery-V 38%
- **σ réalisé intraday** 3.819% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 49% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 93.7952 (VA 93.6422–94.4837 ; dernier close 92.81)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 32% · rebond 79% · **stop −4.7%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 51% (gap-down >1% 34% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.68%) · haut méd +0.89% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.87%) · haut méd +1.24% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.55% (p90 −4.18%) · haut méd +1.72% · range méd 3.56%
- Excursion ouverture 60min (n=160) : bas méd −1.99% (p90 −4.66%) · haut méd +1.74% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 92.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (125/159) · gap 42% · délai 0.0min · rebond 59% (66/125) (MFE +1.42%)
   - −1.0% : fill 30min 64% · séance 71% (111/159) · gap 34% · délai 0.0min · rebond 64% (66/111) (MFE +1.57%)
   - −1.5% : fill 30min 51% · séance 62% (102/159) · gap 23% · délai 0.2min · rebond 59% (58/102) (MFE +1.74%)
   - −2.0% : fill 30min 43% · séance 53% (90/159) · gap 15% · délai 0.5min · rebond 66% (55/90) (MFE +1.47%)
   - −3.0% : fill 30min 32% · séance 43% (68/159) · gap 8% · délai 6.6min · rebond 76% (47/68) (MFE +2.11%)
   - −4.0% : fill 30min 19% · séance 32% (51/159) · gap 4% · délai 11.9min · rebond 79% (34/51) (MFE +2.33%)
   - −5.0% : fill 30min 12% · séance 20% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −2.6%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.44%) → stop au-delà de −1.75% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.47%) → stop au-delà de −1.64% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.14% (p90 −2.87%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 55% (37/70)
      · −2.0% : fill 83% (60/73) · rebond 61% (35/60)
      · −3.0% : fill 71% (49/73) · rebond 73% (33/49)
      · −4.0% : fill 57% (39/73) · rebond 81% (28/39)
      · −5.0% : fill 38% (27/73) · rebond 72% (20/27)
   - **flat** (21 séances) :
      · −1.0% : fill 75% (16/21) · rebond 80% (11/16)
      · −2.0% : fill 47% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 16% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 15% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 7% (3/21) · rebond 82% (2/3)
   - **gap-up** (65 séances) :
      · −1.0% : fill 43% (25/65) · rebond 76% (18/25)
      · −2.0% : fill 24% (18/65) · rebond 88% (13/18)
      · −3.0% : fill 20% (13/65) · rebond 98% (12/13)
      · −4.0% : fill 10% (7/65) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/65) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 63% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 70% si début vert vs 29% si rouge (base 48% · écart 41 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **70%** · continue >prix actuel 51% ; creux résiduel méd -1.79% (q20 -3.27%) → **SL/trailing à −3.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.31% → **scale +1.62% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **29%** (continue à baisser 52%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.07%** (au-delà de la MAE q10 -4.07%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.55% .. +4.1%] · haut q95 +4.55% · bas q05 -5.25%
   - 60min (n=160) : retour [-3.67% .. +4.36%] · haut q95 +5.38% · bas q05 -5.51%
   - 2h (n=160) : retour [-4.72% .. +4.91%] · haut q95 +6.62% · bas q05 -5.99%
   - 4h (n=160) : retour [-4.73% .. +5.83%] · haut q95 +8.15% · bas q05 -6.67%
   - 6h (n=160) : retour [-5.75% .. +6.5%] · haut q95 +8.15% · bas q05 -7.11%
   - session (n=160) : retour [-5.35% .. +6.09%] · haut q95 +8.15% · bas q05 -7.53%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 18% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.12%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=47)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.12%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.08% (q75 +9.69% / q95 +13.38%), MFE méd +6.77% / q90 +14.84%
   - Échelle scale-out : +6.77% (33%) / +11.24% (33%) / +14.84% (34%)
- **DÉSARMER** : repli > **−2.12%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.84% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.61%)


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist -1.25  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 36.8%
- **ATR** : 5.58 (42.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.198  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 43.9  _(transition)_
- **MA** : MA20 99.11 · MA50 98.0 · MA200 98.48  _(prix < MA20)_
- **Dist MA** : MA20 -8.5% · MA50 -7.4% · MA200 -7.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88166 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
