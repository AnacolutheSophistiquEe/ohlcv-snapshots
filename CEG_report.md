# CEG

**Generated** : 2026-08-14T00:28:17.952588+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $278.64  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $278.64 (+1.3% vs entrée) · entrée $275.02 · stop $270.90 · T1 $278.42 · R/R 0.83  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.101 _(réel 5 s)_ (GBM 0.012) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 149 % hors [0,100] (R² max 0.61). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $274.35–$275.70 (mid $275.02)
- Spot actuel : $278.64 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $270.90 (stop swing_plan-based (-6.64%))
- Targets : T1 $278.42 · R/R 0.83 | T2 $281.82 · R/R 1.65 | T3 $285.22 · R/R 2.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $270.90


## Edge, scénarios & sizing

- EV/risk : 0.012 | EV/share : $0.048 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 28 % | T3 8 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.8 | bear 7.2 | side 7.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 279.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.299% → cible +1.235% / stop −1.5%, p_fill 46%, n_eff≈19.9) : P(cible|rempli) **36%** · **EV/risk -0.101** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −2.852% → cible +2.762% / stop −3.9%, p_fill 42%, n_eff≈16.4) : P(cible|rempli) **58%** · **EV/risk -0.009** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −4.407% → cible +3.907% / stop −5.945%, p_fill 42%, n_eff≈18.0) : P(cible|rempli) **65%** · **EV/risk +0.028** (×p_fill ; si rempli +0.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→68% · +2.0%→39% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.39% (p90 5.5%) · excursion haute méd. +1.49% / basse méd. −1.43%
- Profil de vol intra : ouverture 2.502% vs midi 0.681% vs clôture 0.783% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. -0.242% ; recovery-V 10%
- **σ réalisé intraday** 2.354% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 55% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 277.4676 (VA 277.0391–278.7531 ; dernier close 278.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 38% · rebond 60% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 37% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.92%) · haut méd +0.88% · range méd 1.71%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.24%) · haut méd +1.01% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.76%) · haut méd +1.08% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −3.05%) · haut méd +1.3% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 278.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 68% (115/159) · gap 23% · délai 1.2min · rebond 46% (56/115) (MFE +0.93%)
   - −1.0% : fill 30min 43% · séance 59% (101/159) · gap 17% · délai 2.1min · rebond 49% (55/101) (MFE +0.97%)
   - −1.5% : fill 30min 34% · séance 43% (85/159) · gap 10% · délai 3.7min · rebond 49% (45/85) (MFE +0.97%)
   - −2.0% : fill 30min 26% · séance 38% (69/159) · gap 7% · délai 9.2min · rebond 60% (43/69) (MFE +1.08%)
   - −3.0% : fill 30min 10% · séance 23% (42/159) · gap 2% · délai 38.6min · rebond 42% (15/42) (MFE +0.95%)
   - −4.0% : fill 30min 5% · séance 12% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 7% (17/159) · gap 0% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.41%) → stop au-delà de −0.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −1.1%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.37%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=476 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 96% (54/55) · rebond 49% (30/54)
      · −2.0% : fill 76% (42/55) · rebond 58% (27/42)
      · −3.0% : fill 53% (29/55) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/55) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/55) · rebond 77% (11/15)
   - **flat** (28 séances) :
      · −1.0% : fill 57% (16/28) · rebond 34% (5/16)
      · −2.0% : fill 29% (9/28) · rebond 48% (3/9)
      · −3.0% : fill 19% (7/28) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/28) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/28) · rebond 61% (1/2)
   - **gap-up** (76 séances) :
      · −1.0% : fill 38% (31/76) · rebond 56% (20/31)
      · −2.0% : fill 19% (18/76) · rebond 70% (13/18)
      · −3.0% : fill 7% (6/76) · rebond 62% (2/6)
      · −4.0% : fill 2% (3/76) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/76) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 68% si les 15 1res min sont vertes (89 cas) · 27% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 78% si début vert vs 12% si rouge (base 49% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=91) : tient le vert **78%** · continue >prix actuel 49% ; creux résiduel méd -1.01% (q20 -2.21%) → **SL/trailing à −2.21%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.16% / q75 +2.19% → **scale +1.16% / runner +2.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **12%** (continue à baisser 71%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.87%** (au-delà de la MAE q10 -2.87%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.09% .. +2.31%] · haut q95 +2.68% · bas q05 -3.52%
   - 60min (n=160) : retour [-3.72% .. +2.71%] · haut q95 +3.36% · bas q05 -4.7%
   - 2h (n=160) : retour [-3.94% .. +2.98%] · haut q95 +4.17% · bas q05 -5.02%
   - 4h (n=160) : retour [-4.04% .. +3.41%] · haut q95 +4.18% · bas q05 -5.21%
   - 6h (n=160) : retour [-4.76% .. +3.36%] · haut q95 +4.54% · bas q05 -5.21%
   - session (n=160) : retour [-4.33% .. +3.32%] · haut q95 +4.67% · bas q05 -5.92%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 14% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 53.4  _(neutre)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist 1.556  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 12.3%
- **ATR** : 10.56 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.182  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 61.3  _(transition)_
- **MA** : MA20 267.51 · MA50 260.79 · MA200 302.6  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 +6.8% · MA200 -7.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90294 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
