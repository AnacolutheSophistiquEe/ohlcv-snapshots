# IONQ

**Generated** : 2026-07-15T00:26:42.115251+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $39.29  

> 🟡 **WAIT-FOR-DIP** — spot +0.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $39.29 (+0.6% vs entrée) · entrée $39.05 · stop $37.94 · T1 $40.09 · R/R 0.94  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk 0.01 _(réel 5 s)_ (GBM 0.095) · ¼-Kelly 0.026 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.84% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -28 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $38.85–$39.26 (mid $39.05)
- Spot actuel : $39.29 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $37.94 (stop swing_plan-based (-4.26%))
- Targets : T1 $40.09 · R/R 0.94 | T2 $41.12 · R/R 1.86 | T3 $42.16 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $37.94


## Edge, scénarios & sizing

- EV/risk : 0.095 | EV/share : $0.106 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 33 % | T3 33 %
- Kelly (position) : f* 0.106 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.2 | bear 14.1 | side 78.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.604% → cible +2.65% / stop −2.843%, p_fill 87%, n_eff≈35.7) : P(cible|rempli) **52%** · **EV/risk +0.010** (×p_fill ; si rempli +0.03% du capital)
  - **swing** (entrée dip −1.336% → cible +5.926% / stop −2.963%, p_fill 93%, n_eff≈35.9) : P(cible|rempli) **32%** · **EV/risk -0.059** (×p_fill ; si rempli -0.19% du capital)
  - **deep** (entrée dip −2.056% → cible +8.38% / stop −4.19%, p_fill 89%, n_eff≈33.7) : P(cible|rempli) **39%** · **EV/risk +0.073** (×p_fill ; si rempli +0.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→68% · +3.0%→64% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.84% (p90 12.54%) · excursion haute méd. +3.86% / basse méd. −2.98%
- Profil de vol intra : ouverture 5.022% vs midi 1.591% vs clôture 1.667% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; momentum — autocorr 0.047)_ ; drift intra méd. -0.55% ; recovery-V 35%
- **σ réalisé intraday** 5.009% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 67% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 43.4259 (VA 42.9744–43.4259 ; dernier close 42.86)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 82% · **stop −5.07%** sous le fill (sous le bruit) · cible +2.9% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 54% (gap-down >1% 39% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.96%) · haut méd +0.99% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.02%) · haut méd +1.34% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.85% (p90 −5.36%) · haut méd +1.93% · range méd 4.45%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −6.05%) · haut méd +2.5% · range méd 5.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 42.86 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 85% (134/159) · gap 48% · délai 0.0min · rebond 71% (94/134) (MFE +2.24%)
   - −1.0% : fill 30min 72% · séance 81% (126/159) · gap 39% · délai 0.0min · rebond 76% (93/126) (MFE +2.66%)
   - −1.5% : fill 30min 68% · séance 78% (121/159) · gap 32% · délai 0.0min · rebond 73% (85/121) (MFE +2.78%)
   - −2.0% : fill 30min 59% · séance 70% (112/159) · gap 23% · délai 0.2min · rebond 72% (78/112) (MFE +2.7%)
   - −3.0% : fill 30min 48% · séance 60% (92/159) · gap 10% · délai 6.0min · rebond 74% (68/92) (MFE +3.25%)
   - −4.0% : fill 30min 30% · séance 46% (73/159) · gap 5% · délai 18.4min · rebond 76% (55/73) (MFE +2.36%)
   - −5.0% : fill 30min 19% · séance 40% (64/159) · gap 2% · délai 31.2min · rebond 82% (55/64) (MFE +2.9%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.89%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.43%) → stop au-delà de −2.55% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.11% (p90 −3.46%) → stop au-delà de −2.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1117 jambes) : jambe baissière méd −1.31% (p90 −3.3%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 100% (72/72) · rebond 77% (54/72)
      · −2.0% : fill 94% (68/72) · rebond 79% (53/68)
      · −3.0% : fill 82% (58/72) · rebond 76% (45/58)
      · −4.0% : fill 60% (44/72) · rebond 72% (34/44)
      · −5.0% : fill 52% (38/72) · rebond 75% (31/38)
   - **flat** (17 séances) :
      · −1.0% : fill 64% (13/17) · rebond 83% (9/13)
      · −2.0% : fill 48% (12/17) · rebond 48% (6/12)
      · −3.0% : fill 36% (9/17) · rebond 50% (5/9)
      · −4.0% : fill 33% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 33% (7/17) · rebond 91% (6/7)
   - **gap-up** (70 séances) :
      · −1.0% : fill 61% (41/70) · rebond 74% (30/41)
      · −2.0% : fill 46% (32/70) · rebond 57% (19/32)
      · −3.0% : fill 38% (25/70) · rebond 75% (18/25)
      · −4.0% : fill 30% (22/70) · rebond 91% (18/22)
      · −5.0% : fill 25% (19/70) · rebond 99% (18/19)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 55% si les 15 1res min sont vertes (79 cas) · 37% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 78% si début vert vs 20% si rouge (base 47% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -2.18% (q20 -4.23%) → **SL/trailing à −4.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +3.35% → **scale +1.87% / runner +3.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.82%** (au-delà de la MAE q10 -4.82%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +7.16%] · haut q95 +7.86% · bas q05 -5.86%
   - 60min (n=160) : retour [-5.44% .. +5.98%] · haut q95 +9.04% · bas q05 -7.02%
   - 2h (n=160) : retour [-6.58% .. +8.47%] · haut q95 +9.93% · bas q05 -7.53%
   - 4h (n=160) : retour [-7.64% .. +7.61%] · haut q95 +11.7% · bas q05 -8.43%
   - 6h (n=160) : retour [-7.49% .. +7.64%] · haut q95 +11.92% · bas q05 -8.86%
   - session (n=160) : retour [-7.31% .. +9.33%] · haut q95 +11.92% · bas q05 -8.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.6)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.24% (p75 1.9% / p90 2.72%) · ~4.11 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=44)
   - −1.0% → **74%** (reprise méd 20.47 min, n=27)
   - −1.5% → **60%** (reprise méd 38.13 min, n=14)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.72%** (p90, défaut prudent ; serré/agressif −1.9%) ; extension open→close méd +7.82% (q75 +12.53% / q95 +18.2%), MFE méd +9.35% / q90 +18.66%
   - Échelle scale-out : +9.35% (33%) / +13.03% (33%) / +18.66% (34%)
- **DÉSARMER** : repli > **−2.72%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.66% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 17.5  _(survente)_
- **ADX** : 27.4  _(tendance etablie)_
- **MACD** : hist -1.437  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 50.0%
- **ATR** : 3.7 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.425  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 38.6  _(transition)_
- **MA** : MA20 50.54 · MA50 54.9 · MA200 48.69  _(prix < MA20)_
- **Dist MA** : MA20 -22.3% · MA50 -28.4% · MA200 -19.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88179 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
