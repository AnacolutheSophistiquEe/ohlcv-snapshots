# RGTI

**Generated** : 2026-07-17T00:28:57.132371+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $14.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $14.10 (+2.8% vs entrée) · entrée $13.71 · stop $13.27 · T1 $14.57 · R/R 1.95  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.316 _(réel 5 s)_ (GBM 0.122) · ¼-Kelly 0.032 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.16% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -32 % hors [0,100] (R² max 0.44). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $13.64–$13.77 (mid $13.71)
- Spot actuel : $14.10 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : $13.27 (stop swing_plan-based (-8.73%))
- Targets : T1 $14.57 · R/R 1.95 | T2 $14.64 · R/R 2.11 | T3 $14.71 · R/R 2.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $13.27


## Edge, scénarios & sizing

- EV/risk : 0.122 | EV/share : $0.053 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.126 | ¼-Kelly 0.032 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.4 | bear 36.3 | side 55.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.787% → cible +6.323% / stop −3.161%, p_fill 54%, n_eff≈22.0) : P(cible|rempli) **6%** · **EV/risk -0.316** (×p_fill ; si rempli -1.83% du capital)
  - **swing** (entrée dip −6.125% → cible +5.466% / stop −2.775%, p_fill 52%, n_eff≈20.1) : P(cible|rempli) **41%** · **EV/risk +0.067** (×p_fill ; si rempli +0.36% du capital)
  - **deep** (entrée dip −9.461% → cible +7.73% / stop −3.865%, p_fill 45%, n_eff≈17.5) : P(cible|rempli) **20%** · **EV/risk -0.185** (×p_fill ; si rempli -1.60% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→69% · +3.0%→54% · +5.0%→38% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.37% / basse méd. −3.22%
- Profil de vol intra : ouverture 5.346% vs midi 1.676% vs clôture 1.892% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.028)_ ; drift intra méd. -0.588% ; recovery-V 39%
- **σ réalisé intraday** 5.148% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 59% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 15.1822 (VA 15.0733–15.4726 ; dernier close 15.28)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 64% · rebond 76% · **stop −7.22%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.51% · baisse 56% (gap-down >1% 44% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.28% (p90 −2.93%) · haut méd +1.04% · range méd 2.6%
- Excursion ouverture 15min (n=160) : bas méd −1.56% (p90 −4.3%) · haut méd +1.54% · range méd 3.77%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.02%) · haut méd +1.91% · range méd 4.82%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.53%) · haut méd +2.17% · range méd 5.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.28 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 78% · séance 86% (137/159) · gap 50% · délai 0.0min · rebond 66% (89/137) (MFE +2.28%)
   - −1.0% : fill 30min 71% · séance 83% (133/159) · gap 44% · délai 0.0min · rebond 65% (86/133) (MFE +2.03%)
   - −1.5% : fill 30min 65% · séance 77% (125/159) · gap 38% · délai 0.0min · rebond 64% (82/125) (MFE +2.26%)
   - −2.0% : fill 30min 60% · séance 72% (117/159) · gap 28% · délai 0.0min · rebond 64% (76/117) (MFE +2.44%)
   - −3.0% : fill 30min 53% · séance 64% (100/159) · gap 11% · délai 1.5min · rebond 76% (74/100) (MFE +2.55%)
   - −4.0% : fill 30min 38% · séance 48% (79/159) · gap 4% · délai 4.7min · rebond 76% (58/79) (MFE +2.33%)
   - −5.0% : fill 30min 25% · séance 42% (67/159) · gap 2% · délai 20.1min · rebond 71% (51/67) (MFE +1.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.29% (p90 −4.06%) → stop au-delà de −2.32% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.29% (p90 −4.26%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1180 jambes) : jambe baissière méd −1.32% (p90 −3.37%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 63% (50/83)
      · −2.0% : fill 90% (79/84) · rebond 65% (53/79)
      · −3.0% : fill 84% (71/84) · rebond 72% (52/71)
      · −4.0% : fill 65% (57/84) · rebond 74% (42/57)
      · −5.0% : fill 57% (50/84) · rebond 71% (40/50)
   - **flat** (14 séances) :
      · −1.0% : fill 89% (12/14) · rebond 88% (10/12)
      · −2.0% : fill 63% (10/14) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/14) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 61% (38/61) · rebond 64% (26/38)
      · −2.0% : fill 47% (28/61) · rebond 62% (16/28)
      · −3.0% : fill 39% (24/61) · rebond 87% (19/24)
      · −4.0% : fill 24% (17/61) · rebond 82% (13/17)
      · −5.0% : fill 20% (12/61) · rebond 66% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 64% si les 15 1res min sont vertes (79 cas) · 35% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 88% si début vert vs 17% si rouge (base 50% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 177min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **88%** · continue >prix actuel 54% ; creux résiduel méd -2.21% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.75% / q75 +4.27% → **scale +2.75% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **17%** (continue à baisser 56%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.74%** (au-delà de la MAE q10 -5.74%), cible rebond +2.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.45% .. +4.87%] · haut q95 +7.55% · bas q05 -6.76%
   - 60min (n=160) : retour [-6.08% .. +7.14%] · haut q95 +9.09% · bas q05 -7.16%
   - 2h (n=160) : retour [-7.5% .. +8.06%] · haut q95 +9.24% · bas q05 -8.2%
   - 4h (n=160) : retour [-8.41% .. +6.52%] · haut q95 +9.24% · bas q05 -10.12%
   - 6h (n=160) : retour [-8.55% .. +8.32%] · haut q95 +9.56% · bas q05 -10.4%
   - session (n=160) : retour [-7.84% .. +9.58%] · haut q95 +10.73% · bas q05 -10.42%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 10% vs absente 1% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.86% / p90 2.75%) · ~4.0 replis/séance, durée méd 35.49 min. P(nouveau plus-haut après repli) :
   - −0.5% → **93%** (reprise méd 10.0 min, n=40)
   - −1.0% → **90%** (reprise méd 30.5 min, n=25)
   - −1.5% → **81%** (reprise méd 42.31 min, n=11)
   - −2.0% → **69%** (reprise méd 145.0 min, n=7)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.75%** (p90, défaut prudent ; serré/agressif −1.86%) ; extension open→close méd +8.26% (q75 +9.93% / q95 +13.03%), MFE méd +8.98% / q90 +12.5%
   - Échelle scale-out : +8.98% (33%) / +10.45% (33%) / +12.5% (34%)
- **DÉSARMER** : repli > **−2.75%** depuis le plus-haut = décay → P(retournement) **74%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.5% : P(retournement après) 0% (mèche méd 0.52%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.96%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.8  _(survente)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist -0.375  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 46.8%
- **ATR** : 1.22 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.217  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 40.6  _(transition)_
- **MA** : MA20 18.09 · MA50 20.0 · MA200 23.36  _(prix < MA20)_
- **Dist MA** : MA20 -22.0% · MA50 -29.5% · MA200 -39.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87978 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
