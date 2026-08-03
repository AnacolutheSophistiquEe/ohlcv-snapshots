# IONQ

**Generated** : 2026-08-03T22:02:59.835302+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $38.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)  
> ↳ spot $38.85 (+2.9% vs entrée) · entrée $37.76 · stop $36.92 · T1 $38.88 · R/R 1.33  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk -0.242 _(réel 5 s)_ (GBM 0.067) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.23% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $37.53–$37.98 (mid $37.76)
- Spot actuel : $38.85 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $36.92 (stop swing_plan-based (-13.41%))
- Targets : T1 $38.88 · R/R 1.33 | T2 $40.01 · R/R 2.68 | T3 $41.15 · R/R 4.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $36.92


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : $0.056 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 28 % | T3 28 %
- Kelly (position) : f* 0.089 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 53.4 | bear 36.5 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.816% → cible +2.983% / stop −2.227%, p_fill 50%, n_eff≈21.9) : P(cible|rempli) **16%** · **EV/risk -0.242** (×p_fill ; si rempli -1.09% du capital)
  - **swing** (entrée dip −6.196% → cible +6.694% / stop −7.69%, p_fill 46%, n_eff≈19.3) : P(cible|rempli) **33%** · **EV/risk -0.142** (×p_fill ; si rempli -2.38% du capital)
  - **deep** (entrée dip −9.569% → cible +9.467% / stop −11.966%, p_fill 59%, n_eff≈21.6) : P(cible|rempli) **27%** · **EV/risk -0.217** (×p_fill ; si rempli -4.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→62% · +5.0%→32% · +8.0%→16%
- Range intraday médian 7.76% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −2.98%
- Profil de vol intra : ouverture 5.242% vs midi 1.575% vs clôture 1.69% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr 0.018)_ ; drift intra méd. -0.787% ; recovery-V 27%
- **σ réalisé intraday** 4.73% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 70% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 36.3872 (VA 36.0902–36.5853 ; dernier close 36.43)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 54% (gap-down >1% 38% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.25% (p90 −2.91%) · haut méd +1.11% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.64% (p90 −4.19%) · haut méd +1.34% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.89% (p90 −5.27%) · haut méd +1.78% · range méd 4.5%
- Excursion ouverture 60min (n=160) : bas méd −2.48% (p90 −5.94%) · haut méd +2.24% · range méd 5.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.43 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 82% (134/159) · gap 45% · délai 0.0min · rebond 68% (92/134) (MFE +1.89%)
   - −1.0% : fill 30min 69% · séance 78% (127/159) · gap 38% · délai 0.0min · rebond 73% (93/127) (MFE +2.35%)
   - −1.5% : fill 30min 66% · séance 76% (122/159) · gap 31% · délai 0.0min · rebond 66% (83/122) (MFE +2.51%)
   - −2.0% : fill 30min 58% · séance 68% (112/159) · gap 19% · délai 0.3min · rebond 66% (76/112) (MFE +2.53%)
   - −3.0% : fill 30min 48% · séance 58% (93/159) · gap 9% · délai 7.7min · rebond 72% (67/93) (MFE +2.8%)
   - −4.0% : fill 30min 30% · séance 46% (74/159) · gap 6% · délai 16.7min · rebond 72% (55/74) (MFE +2.19%)
   - −5.0% : fill 30min 20% · séance 40% (64/159) · gap 2% · délai 31.1min · rebond 83% (55/64) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.83% (p90 −2.88%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.98% (p90 −3.52%) → stop au-delà de −2.43% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.97% (p90 −2.87%) → stop au-delà de −2.33% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1124 jambes) : jambe baissière méd −1.33% (p90 −3.19%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 73% (56/75)
      · −2.0% : fill 95% (71/75) · rebond 71% (53/71)
      · −3.0% : fill 83% (61/75) · rebond 70% (45/61)
      · −4.0% : fill 63% (46/75) · rebond 69% (34/46)
      · −5.0% : fill 56% (40/75) · rebond 77% (32/40)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 52% (39/68) · rebond 71% (28/39)
      · −2.0% : fill 36% (29/68) · rebond 52% (17/29)
      · −3.0% : fill 31% (23/68) · rebond 78% (17/23)
      · −4.0% : fill 25% (20/68) · rebond 79% (17/20)
      · −5.0% : fill 22% (17/68) · rebond 100% (17/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 51% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 77% si début vert vs 17% si rouge (base 42% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 55% ; creux résiduel méd -2.19% (q20 -3.67%) → **SL/trailing à −3.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.88% / q75 +3.24% → **scale +1.88% / runner +3.24%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.24%** (au-delà de la MAE q10 -4.24%), cible rebond +2.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +6.64%] · haut q95 +7.82% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.17% .. +5.75%] · haut q95 +8.28% · bas q05 -6.71%
   - 2h (n=160) : retour [-6.39% .. +7.84%] · haut q95 +8.82% · bas q05 -7.28%
   - 4h (n=160) : retour [-7.25% .. +7.0%] · haut q95 +10.1% · bas q05 -8.28%
   - 6h (n=160) : retour [-7.49% .. +7.64%] · haut q95 +10.1% · bas q05 -8.54%
   - session (n=160) : retour [-7.32% .. +8.06%] · haut q95 +10.1% · bas q05 -8.54%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.89% / p90 2.79%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=39)
   - −1.0% → **74%** (reprise méd 20.0 min, n=24)
   - −1.5% → **59%** (reprise méd 38.13 min, n=12)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.79%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +7.79% (q75 +10.75% / q95 +18.2%), MFE méd +9.27% / q90 +19.18%
   - Échelle scale-out : +9.27% (33%) / +12.82% (33%) / +19.18% (34%)
- **DÉSARMER** : repli > **−2.79%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +19.18% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 49.0  _(neutre)_
- **ADX** : 37.1  _(tendance etablie)_
- **MACD** : hist 0.838  _(bullish_recent)_
- **BB** : %B 0.59 · largeur 44.4%
- **ATR** : 2.8 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.258  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 58.6  _(transition)_
- **MA** : MA20 37.39 · MA50 50.39 · MA200 46.1  _(prix > MA20)_
- **Dist MA** : MA20 +3.9% · MA50 -22.9% · MA200 -15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88909 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
