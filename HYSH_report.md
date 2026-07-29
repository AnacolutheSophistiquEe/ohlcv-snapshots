# 298040

**Generated** : 2026-07-29T21:52:01.510027+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1990000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩1990000.00 (+7.2% vs entrée) · entrée ₩1856355.88 · stop ₩1674533.82 · T1 ₩2220000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.012 _(réel 5 s)_ (GBM 0.126) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -123 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1824857.01–₩1887854.75 (mid ₩1856355.88)
- Spot actuel : ₩1990000.00 (+7.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1674533.82 (stop swing_plan-based (-15.85%))
- Targets : T1 ₩2220000.00 · R/R 2.0 | T2 ₩2273703.59 · R/R 2.3 | T3 ₩2327407.18 · R/R 2.59
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1674533.82


## Edge, scénarios & sizing

- EV/risk : 0.126 | EV/share : ₩22927.417 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 5 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.8 | bear 67.2 | side 15.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.05% → cible +8.128% / stop −4.064%, p_fill 72%, n_eff≈28.3) : P(cible|rempli) **0%** · **EV/risk -0.131** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −6.713% → cible +19.589% / stop −9.795%, p_fill 45%, n_eff≈18.1) : P(cible|rempli) **10%** · **EV/risk -0.012** (×p_fill ; si rempli -0.27% du capital)
  - **deep** (entrée dip −10.38% → cible +11.962% / stop −5.981%, p_fill 52%, n_eff≈18.5) : P(cible|rempli) **30%** · **EV/risk -0.093** (×p_fill ; si rempli -1.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→52% · +3.0%→39% · +5.0%→22% · +8.0%→6%
- Range intraday médian 6.97% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.93%
- Profil de vol intra : ouverture 4.296% vs midi 1.076% vs clôture 1.166% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.095)_ ; drift intra méd. -1.838% ; recovery-V 27%
- **σ réalisé intraday** 5.111% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 68% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 2386762.5 (VA 2332012.5–2419612.5 ; dernier close 2317000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 82% · **stop −5.69%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.41 (high win-rate)
- Gaps overnight (n=141) : méd. 0.6% · baisse 38% (gap-down >1% 24% · >2% 18%)
- Excursion ouverture 5min (n=142) : bas méd −1.29% (p90 −3.44%) · haut méd +0.81% · range méd 2.71%
- Excursion ouverture 15min (n=142) : bas méd −2.08% (p90 −4.45%) · haut méd +1.02% · range méd 3.65%
- Excursion ouverture 30min (n=142) : bas méd −2.47% (p90 −4.9%) · haut méd +1.11% · range méd 4.17%
- Excursion ouverture 60min (n=142) : bas méd −2.69% (p90 −5.29%) · haut méd +1.34% · range méd 4.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2317000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (97/141) · gap 33% · délai 0.0min · rebond 60% (60/97) (MFE +1.27%)
   - −1.0% : fill 30min 57% · séance 68% (89/141) · gap 24% · délai 0.6min · rebond 60% (55/89) (MFE +1.55%)
   - −1.5% : fill 30min 50% · séance 61% (80/141) · gap 21% · délai 1.3min · rebond 52% (48/80) (MFE +1.28%)
   - −2.0% : fill 30min 45% · séance 58% (71/141) · gap 18% · délai 4.0min · rebond 51% (38/71) (MFE +1.07%)
   - −3.0% : fill 30min 34% · séance 49% (58/141) · gap 9% · délai 6.8min · rebond 53% (32/58) (MFE +1.03%)
   - −4.0% : fill 30min 23% · séance 44% (50/141) · gap 6% · délai 26.3min · rebond 71% (37/50) (MFE +1.89%)
   - −5.0% : fill 30min 19% · séance 35% (37/141) · gap 6% · délai 22.7min · rebond 82% (30/37) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.19%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −4.17%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −4.2%) → stop au-delà de −2.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=762 jambes) : jambe baissière méd −1.4% (p90 −3.4%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 100% (49/49) · rebond 56% (30/49)
      · −2.0% : fill 88% (41/49) · rebond 51% (22/41)
      · −3.0% : fill 84% (39/49) · rebond 51% (21/39)
      · −4.0% : fill 80% (34/49) · rebond 74% (25/34)
      · −5.0% : fill 68% (28/49) · rebond 83% (22/28)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (76 séances) :
      · −1.0% : fill 44% (29/76) · rebond 63% (17/29)
      · −2.0% : fill 34% (22/76) · rebond 48% (11/22)
      · −3.0% : fill 24% (14/76) · rebond 52% (7/14)
      · −4.0% : fill 19% (11/76) · rebond 76% (9/11)
      · −5.0% : fill 10% (6/76) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 37% en base · 61% si les 15 1res min sont vertes (57 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 37% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.65% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.18% → **scale +1.7% / runner +3.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **13%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.79%** (au-delà de la MAE q10 -4.79%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-4.26% .. +4.23%] · haut q95 +6.06% · bas q05 -5.24%
   - 60min (n=142) : retour [-5.25% .. +4.77%] · haut q95 +6.25% · bas q05 -5.57%
   - 2h (n=142) : retour [-6.96% .. +4.37%] · haut q95 +6.69% · bas q05 -8.01%
   - 4h (n=142) : retour [-7.53% .. +5.28%] · haut q95 +7.2% · bas q05 -9.25%
   - 6h (n=142) : retour [-7.6% .. +5.24%] · haut q95 +8.14% · bas q05 -9.3%
   - session (n=142) : retour [-6.92% .. +5.54%] · haut q95 +8.14% · bas q05 -9.39%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 24% vs absente 0% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.3  _(momentum baissier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist -44182.936  _(pas de croisement recent)_
- **BB** : %B -0.04 · largeur 54.3%
- **ATR** : 260785.71 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 1.68  _(volume au-dessus de la moyenne)_
- **Choppiness** : 45.1  _(transition)_
- **MA** : MA20 2807850.0 · MA50 3274300.0 · MA200 2635933.13  _(prix < MA20)_
- **Dist MA** : MA20 -29.1% · MA50 -39.2% · MA200 -24.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88248 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
