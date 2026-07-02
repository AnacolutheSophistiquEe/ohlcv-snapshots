# HOOD

**Generated** : 2026-07-02T00:23:57.152059+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $108.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $108.65 (+2.6% vs entrée) · entrée $105.91 · stop $102.73 · T1 $108.72 · R/R 0.88  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.056 _(réel 5 s)_ (GBM 0.003) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 130 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $105.34–$106.47 (mid $105.91)
- Spot actuel : $108.65 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : $102.73 (stop swing_plan-based (-8.36%))
- Targets : T1 $108.72 · R/R 0.88 | T2 $111.53 · R/R 1.77 | T3 $114.34 · R/R 2.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $102.73


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 68.2 | bear 14.3 | side 17.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 543.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.526% → cible +2.656% / stop −3.0%, p_fill 45%, n_eff≈18.4) : P(cible|rempli) **34%** · **EV/risk -0.056** (×p_fill ; si rempli -0.38% du capital)
  - **swing** (entrée dip −5.555% → cible +5.939% / stop −2.97%, p_fill 28%, n_eff≈9.3) : P(cible|rempli) **49%** · **EV/risk +0.105** (×p_fill ; si rempli +1.14% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→51% · +3.0%→34% · +5.0%→16% · +8.0%→5%
- Range intraday médian 4.84% (p90 8.55%) · excursion haute méd. +2.05% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.32% vs midi 1.065% vs clôture 1.027% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 65% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; momentum — autocorr 0.054)_ ; drift intra méd. 0.539% ; recovery-V 40%
- **σ réalisé intraday** 3.647% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 45% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 100.7212 (VA 100.3088–101.7113 ; dernier close 100.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 21% · rebond 85% · **stop −4.8%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.93%) · haut méd +0.78% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.01%) · haut méd +0.99% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.79%) · haut méd +1.13% · range méd 3.06%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −3.86%) · haut méd +1.49% · range méd 3.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 100.27 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (121/159) · gap 40% · délai 0.0min · rebond 55% (61/121) (MFE +1.41%)
   - −1.0% : fill 30min 57% · séance 65% (106/159) · gap 32% · délai 0.0min · rebond 57% (59/106) (MFE +1.27%)
   - −1.5% : fill 30min 49% · séance 61% (99/159) · gap 23% · délai 0.2min · rebond 52% (53/99) (MFE +1.22%)
   - −2.0% : fill 30min 42% · séance 57% (90/159) · gap 17% · délai 1.0min · rebond 62% (53/90) (MFE +1.3%)
   - −3.0% : fill 30min 32% · séance 42% (68/159) · gap 8% · délai 10.7min · rebond 66% (43/68) (MFE +1.69%)
   - −4.0% : fill 30min 20% · séance 33% (52/159) · gap 4% · délai 12.3min · rebond 74% (33/52) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 21% (34/159) · gap 2% · délai 21.5min · rebond 85% (27/34) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.61%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.53%) → stop au-delà de −1.78% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.46%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=749 jambes) : jambe baissière méd −1.16% (p90 −2.72%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (66/70) · rebond 52% (34/66)
      · −2.0% : fill 85% (57/70) · rebond 56% (32/57)
      · −3.0% : fill 71% (46/70) · rebond 61% (28/46)
      · −4.0% : fill 58% (38/70) · rebond 79% (27/38)
      · −5.0% : fill 42% (28/70) · rebond 84% (23/28)
   - **flat** (22 séances) :
      · −1.0% : fill 66% (16/22) · rebond 71% (11/16)
      · −2.0% : fill 61% (12/22) · rebond 59% (7/12)
      · −3.0% : fill 21% (6/22) · rebond 23% (2/6)
      · −4.0% : fill 19% (5/22) · rebond 16% (1/5)
      · −5.0% : fill 9% (3/22) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 34% (24/67) · rebond 63% (14/24)
      · −2.0% : fill 28% (21/67) · rebond 82% (14/21)
      · −3.0% : fill 22% (16/67) · rebond 93% (13/16)
      · −4.0% : fill 12% (9/67) · rebond 80% (5/9)
      · −5.0% : fill 4% (3/67) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 72% si les 15 1res min sont vertes (70 cas) · 38% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 90% si début vert vs 19% si rouge (base 52% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **90%** · continue >prix actuel 57% ; creux résiduel méd -1.26% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.01% / q75 +3.13% → **scale +1.01% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **19%** (continue à baisser 60%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.49% .. +3.9%] · haut q95 +4.3% · bas q05 -4.52%
   - 60min (n=160) : retour [-3.65% .. +4.93%] · haut q95 +5.16% · bas q05 -4.83%
   - 2h (n=160) : retour [-4.09% .. +4.64%] · haut q95 +7.37% · bas q05 -5.57%
   - 4h (n=160) : retour [-4.66% .. +5.96%] · haut q95 +8.56% · bas q05 -6.14%
   - 6h (n=160) : retour [-5.5% .. +6.71%] · haut q95 +8.56% · bas q05 -6.75%
   - session (n=160) : retour [-5.03% .. +6.23%] · haut q95 +8.56% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **42%**. Lecture précoce 30 min : signature présente → 21% vs absente 5% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.42% / p90 2.29%) · ~3.81 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **84%** (reprise méd 20.0 min, n=49)
   - −1.0% → **67%** (reprise méd 30.0 min, n=22)
   - −1.5% → **32%** (reprise méd 35.94 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.29%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.1% (q75 +9.8% / q95 +13.38%), MFE méd +7.16% / q90 +15.08%
   - Échelle scale-out : +7.16% (33%) / +12.41% (33%) / +15.08% (34%)
- **DÉSARMER** : repli > **−2.29%** depuis le plus-haut = décay → P(retournement) **71%** (préavis méd 134.36 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.08% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 75% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 69.4  _(momentum haussier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist 0.268  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 36.0%
- **ATR** : 7.12 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.024  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 49.8  _(transition)_
- **MA** : MA20 95.57 · MA50 86.06 · MA200 102.38  _(prix > MA20)_
- **Dist MA** : MA20 +13.7% · MA50 +26.3% · MA200 +6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94385 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
