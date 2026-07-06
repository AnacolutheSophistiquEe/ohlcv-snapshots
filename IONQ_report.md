# IONQ

**Generated** : 2026-07-06T21:51:53.874552+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $48.87  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $48.87 (+2.9% vs entrée) · entrée $47.50 · stop $46.08 · T1 $49.11 · R/R 1.13  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.073 _(réel 5 s)_ (GBM 0.115) · ¼-Kelly 0.035 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.80). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $47.18–$47.82 (mid $47.50)
- Spot actuel : $48.87 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $46.08 (stop swing_plan-based (-9.72%))
- Targets : T1 $49.11 · R/R 1.13 | T2 $50.72 · R/R 2.27 | T3 $52.33 · R/R 3.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $46.08


## Edge, scénarios & sizing

- EV/risk : 0.115 | EV/share : $0.163 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.139 | ¼-Kelly 0.035 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.9 | bear 27.1 | side 62.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 147.0 (= 3 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.804% → cible +3.391% / stop −3.0%, p_fill 53%, n_eff≈21.8) : P(cible|rempli) **36%** · **EV/risk -0.073** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −6.162% → cible +7.583% / stop −3.791%, p_fill 43%, n_eff≈16.8) : P(cible|rempli) **21%** · **EV/risk -0.189** (×p_fill ; si rempli -1.66% du capital)
  - **deep** (entrée dip −9.529% → cible +10.724% / stop −5.362%, p_fill 40%, n_eff≈14.5) : P(cible|rempli) **41%** · **EV/risk +0.076** (×p_fill ; si rempli +1.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→70% · +3.0%→62% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.82% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −2.97%
- Profil de vol intra : ouverture 4.927% vs midi 1.597% vs clôture 1.681% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; momentum — autocorr 0.04)_ ; drift intra méd. -0.111% ; recovery-V 38%
- **σ réalisé intraday** 5.326% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 59% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 48.8941 (VA 48.4314–50.4366 ; dernier close 49.16)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 86% · **stop −4.72%** sous le fill (sous le bruit) · cible +3.14% · R/R 0.67 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 54% (gap-down >1% 39% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −3.01%) · haut méd +1.0% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.63% (p90 −3.91%) · haut méd +1.34% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.87% (p90 −5.21%) · haut méd +1.96% · range méd 4.49%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −5.86%) · haut méd +2.59% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 49.16 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (133/159) · gap 49% · délai 0.0min · rebond 73% (94/133) (MFE +2.26%)
   - −1.0% : fill 30min 73% · séance 81% (126/159) · gap 39% · délai 0.0min · rebond 79% (94/126) (MFE +2.76%)
   - −1.5% : fill 30min 69% · séance 78% (121/159) · gap 32% · délai 0.0min · rebond 75% (86/121) (MFE +2.8%)
   - −2.0% : fill 30min 58% · séance 72% (113/159) · gap 21% · délai 0.3min · rebond 75% (81/113) (MFE +2.87%)
   - −3.0% : fill 30min 48% · séance 60% (91/159) · gap 11% · délai 5.1min · rebond 75% (68/91) (MFE +3.44%)
   - −4.0% : fill 30min 28% · séance 46% (73/159) · gap 5% · délai 18.4min · rebond 79% (56/73) (MFE +2.49%)
   - −5.0% : fill 30min 19% · séance 40% (64/159) · gap 3% · délai 31.2min · rebond 86% (56/64) (MFE +3.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.02% (p90 −2.89%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.11% (p90 −3.49%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.14% (p90 −3.53%) → stop au-delà de −2.64% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1114 jambes) : jambe baissière méd −1.34% (p90 −3.29%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 100% (72/72) · rebond 78% (54/72)
      · −2.0% : fill 94% (68/72) · rebond 82% (54/68)
      · −3.0% : fill 81% (58/72) · rebond 74% (45/58)
      · −4.0% : fill 61% (45/72) · rebond 77% (36/45)
      · −5.0% : fill 52% (39/72) · rebond 81% (33/39)
   - **flat** (16 séances) :
      · −1.0% : fill 78% (13/16) · rebond 83% (9/13)
      · −2.0% : fill 59% (12/16) · rebond 48% (6/12)
      · −3.0% : fill 44% (9/16) · rebond 50% (5/9)
      · −4.0% : fill 40% (7/16) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/16) · rebond 91% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 57% (41/71) · rebond 78% (31/41)
      · −2.0% : fill 45% (33/71) · rebond 64% (21/33)
      · −3.0% : fill 36% (24/71) · rebond 86% (18/24)
      · −4.0% : fill 27% (21/71) · rebond 89% (17/21)
      · −5.0% : fill 22% (18/71) · rebond 98% (17/18)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 57% si les 15 1res min sont vertes (80 cas) · 41% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 50% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **80%** · continue >prix actuel 56% ; creux résiduel méd -2.16% (q20 -3.96%) → **SL/trailing à −3.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.98% / q75 +3.39% → **scale +1.98% / runner +3.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 53%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.43%** (au-delà de la MAE q10 -5.43%), cible rebond +2.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.13% .. +7.16%] · haut q95 +8.06% · bas q05 -5.88%
   - 60min (n=160) : retour [-5.19% .. +6.1%] · haut q95 +10.11% · bas q05 -6.75%
   - 2h (n=160) : retour [-6.61% .. +8.5%] · haut q95 +10.81% · bas q05 -7.54%
   - 4h (n=160) : retour [-7.66% .. +7.71%] · haut q95 +12.09% · bas q05 -8.5%
   - 6h (n=160) : retour [-7.52% .. +7.64%] · haut q95 +12.41% · bas q05 -9.38%
   - session (n=160) : retour [-7.38% .. +9.46%] · haut q95 +12.43% · bas q05 -8.88%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 12% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.91% / p90 2.69%) · ~4.38 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=47)
   - −1.0% → **74%** (reprise méd 20.0 min, n=29)
   - −1.5% → **60%** (reprise méd 36.27 min, n=15)
   - −2.0% → **52%** (reprise méd 29.52 min, n=9)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.69%** (p90, défaut prudent ; serré/agressif −1.91%) ; extension open→close méd +7.85% (q75 +12.44% / q95 +18.2%), MFE méd +9.42% / q90 +18.49%
   - Échelle scale-out : +9.42% (33%) / +13.0% (33%) / +18.49% (34%)
- **DÉSARMER** : repli > **−2.69%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.49% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +1.02%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 19.8  _(pas de tendance nette)_
- **MACD** : hist -1.117  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 28.3%
- **ATR** : 4.55 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.359  _(distribution)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 55.17 · MA50 54.99 · MA200 49.53  _(prix < MA20)_
- **Dist MA** : MA20 -11.4% · MA50 -11.1% · MA200 -1.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93480 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
