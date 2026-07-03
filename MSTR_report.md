# MSTR

**Generated** : 2026-07-03T00:12:57.695594+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $100.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $100.77 (+11.2% vs entrée) · entrée $90.63 · stop $83.38 · T1 $93.87 · R/R 0.45  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.085 · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $89.99–$91.28 (mid $90.63)
- Spot actuel : $100.77 (+11.2% au-dessus de la zone — repli à attendre)
- Stop : $83.38 (stop swing_plan-based (-23.3%))
- Targets : T1 $93.87 · R/R 0.45 | T2 $97.10 · R/R 0.89 | T3 $100.34 · R/R 1.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $83.38


## Edge, scénarios & sizing

- EV/risk : -0.085 | EV/share : $-0.614 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 56.5 | bear 37.4 | side 6.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→52% · +3.0%→34% · +5.0%→12% · +8.0%→6%
- Range intraday médian 5.22% (p90 9.51%) · excursion haute méd. +2.32% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.232% vs midi 1.214% vs clôture 1.256% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; neutre — autocorr -0.002)_ ; drift intra méd. -0.995% ; recovery-V 37%
- **σ réalisé intraday** 4.191% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 75% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 97.0942 (VA 94.6662–98.3082 ; dernier close 93.39)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 65% · **stop −5.32%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.23 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 55% (gap-down >1% 40% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.98% (p90 −2.06%) · haut méd +0.61% · range méd 1.85%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −3.02%) · haut méd +0.87% · range méd 2.53%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.69%) · haut méd +1.12% · range méd 3.11%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −4.96%) · haut méd +1.47% · range méd 3.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.39 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (127/159) · gap 47% · délai 0.0min · rebond 48% (63/127) (MFE +0.96%)
   - −1.0% : fill 30min 64% · séance 76% (121/159) · gap 40% · délai 0.0min · rebond 54% (68/121) (MFE +1.34%)
   - −1.5% : fill 30min 57% · séance 72% (113/159) · gap 29% · délai 0.0min · rebond 54% (67/113) (MFE +1.2%)
   - −2.0% : fill 30min 49% · séance 64% (101/159) · gap 25% · délai 0.9min · rebond 54% (64/101) (MFE +1.17%)
   - −3.0% : fill 30min 34% · séance 53% (77/159) · gap 15% · délai 7.7min · rebond 51% (46/77) (MFE +1.39%)
   - −4.0% : fill 30min 22% · séance 46% (63/159) · gap 7% · délai 36.8min · rebond 53% (37/63) (MFE +1.05%)
   - −5.0% : fill 30min 17% · séance 34% (48/159) · gap 4% · délai 30.0min · rebond 65% (34/48) (MFE +1.25%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.72%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −2.83%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.27% (p90 −3.14%) → stop au-delà de −2.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=964 jambes) : jambe baissière méd −1.21% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 46% (36/73)
      · −2.0% : fill 89% (66/74) · rebond 48% (38/66)
      · −3.0% : fill 79% (57/74) · rebond 52% (34/57)
      · −4.0% : fill 68% (47/74) · rebond 54% (30/47)
      · −5.0% : fill 55% (38/74) · rebond 66% (28/38)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 45% (32/68) · rebond 63% (22/32)
      · −2.0% : fill 34% (22/68) · rebond 72% (17/22)
      · −3.0% : fill 22% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 20% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 10% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 48% si les 15 1res min sont vertes (72 cas) · 39% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 69% si début vert vs 22% si rouge (base 43% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 210min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **69%** · continue >prix actuel 47% ; creux résiduel méd -1.9% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +3.34% → **scale +1.9% / runner +3.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.71%** (au-delà de la MAE q10 -5.71%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +3.93%] · haut q95 +4.71% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.08% .. +3.49%] · haut q95 +5.3% · bas q05 -5.53%
   - 2h (n=160) : retour [-4.78% .. +5.57%] · haut q95 +6.47% · bas q05 -5.58%
   - 4h (n=160) : retour [-7.59% .. +7.41%] · haut q95 +8.76% · bas q05 -8.32%
   - 6h (n=160) : retour [-7.17% .. +6.66%] · haut q95 +9.35% · bas q05 -8.5%
   - session (n=160) : retour [-6.09% .. +6.44%] · haut q95 +9.35% · bas q05 -8.5%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.2  _(momentum baissier)_
- **ADX** : 30.4  _(tendance etablie)_
- **MACD** : hist -0.042  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 57.4%
- **ATR** : 10.14 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.225  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 36.3  _(marche directionnel)_
- **MA** : MA20 109.27 · MA50 145.02 · MA200 181.26  _(prix < MA20)_
- **Dist MA** : MA20 -7.8% · MA50 -30.5% · MA200 -44.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87506 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
