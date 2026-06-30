# HOOD

**Generated** : 2026-06-30T21:58:50.554093+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $100.28  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $100.28 (+0.7% vs entrée) · entrée $99.63 · stop $96.64 · T1 $103.15 · R/R 1.18  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.12 _(réel 5 s)_ (GBM 0.026) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $99.12–$100.13 (mid $99.63)
- Spot actuel : $100.28 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : $96.64 (stop swing_plan-based (-4.23%))
- Targets : T1 $103.15 · R/R 1.18 | T2 $105.18 · R/R 1.86 | T3 $107.21 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $96.64


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : $0.077 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 67.7 | bear 17.0 | side 15.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 301.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.649% → cible +3.539% / stop −3.0%, p_fill 78%, n_eff≈33.6) : P(cible|rempli) **22%** · **EV/risk -0.120** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −1.435% → cible +5.672% / stop −2.836%, p_fill 82%, n_eff≈32.8) : P(cible|rempli) **40%** · **EV/risk +0.180** (×p_fill ; si rempli +0.62% du capital)
  - **deep** (entrée dip −2.208% → cible +8.022% / stop −4.011%, p_fill 78%, n_eff≈31.8) : P(cible|rempli) **46%** · **EV/risk +0.325** (×p_fill ; si rempli +1.67% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→51% · +3.0%→34% · +5.0%→16% · +8.0%→5%
- Range intraday médian 4.84% (p90 8.55%) · excursion haute méd. +2.05% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.335% vs midi 1.063% vs clôture 1.03% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑1%/↓0% ; spike-down 64% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; momentum — autocorr 0.052)_ ; drift intra méd. 0.638% ; recovery-V 42%
- **σ réalisé intraday** 3.687% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 42% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 101.6866 (VA 100.3859–102.6326 ; dernier close 101.83)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 85% · **stop −4.8%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.07% · baisse 53% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −1.95%) · haut méd +0.8% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.16% (p90 −3.02%) · haut méd +1.02% · range méd 2.57%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.81%) · haut méd +1.25% · range méd 3.12%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −3.87%) · haut méd +1.53% · range méd 3.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 101.83 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (121/159) · gap 40% · délai 0.0min · rebond 54% (61/121) (MFE +1.37%)
   - −1.0% : fill 30min 56% · séance 64% (105/159) · gap 32% · délai 0.0min · rebond 56% (58/105) (MFE +1.26%)
   - −1.5% : fill 30min 50% · séance 61% (98/159) · gap 24% · délai 0.1min · rebond 51% (52/98) (MFE +1.12%)
   - −2.0% : fill 30min 43% · séance 56% (89/159) · gap 17% · délai 0.6min · rebond 61% (52/89) (MFE +1.28%)
   - −3.0% : fill 30min 32% · séance 43% (68/159) · gap 9% · délai 10.7min · rebond 66% (43/68) (MFE +1.69%)
   - −4.0% : fill 30min 21% · séance 34% (52/159) · gap 4% · délai 12.3min · rebond 74% (33/52) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 22% (34/159) · gap 2% · délai 21.5min · rebond 85% (27/34) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.61%) → stop au-delà de −1.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.53%) → stop au-delà de −1.78% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.46%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.15% (p90 −2.73%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (66/70) · rebond 52% (34/66)
      · −2.0% : fill 85% (57/70) · rebond 56% (32/57)
      · −3.0% : fill 71% (46/70) · rebond 61% (28/46)
      · −4.0% : fill 58% (38/70) · rebond 79% (27/38)
      · −5.0% : fill 42% (28/70) · rebond 84% (23/28)
   - **flat** (21 séances) :
      · −1.0% : fill 61% (15/21) · rebond 64% (10/15)
      · −2.0% : fill 55% (11/21) · rebond 48% (6/11)
      · −3.0% : fill 24% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 22% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 11% (3/21) · rebond 82% (2/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 34% (24/68) · rebond 63% (14/24)
      · −2.0% : fill 28% (21/68) · rebond 82% (14/21)
      · −3.0% : fill 22% (16/68) · rebond 93% (13/16)
      · −4.0% : fill 12% (9/68) · rebond 80% (5/9)
      · −5.0% : fill 4% (3/68) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 72% si les 15 1res min sont vertes (70 cas) · 39% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 92% si début vert vs 22% si rouge (base 54% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **92%** · continue >prix actuel 64% ; creux résiduel méd -1.16% (q20 -2.08%) → **SL/trailing à −2.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.75% / q75 +3.29% → **scale +1.75% / runner +3.29%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 58%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.28%** (au-delà de la MAE q10 -4.28%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.49% .. +3.9%] · haut q95 +4.33% · bas q05 -4.56%
   - 60min (n=160) : retour [-3.65% .. +4.93%] · haut q95 +5.16% · bas q05 -4.85%
   - 2h (n=160) : retour [-4.09% .. +4.78%] · haut q95 +7.46% · bas q05 -5.57%
   - 4h (n=160) : retour [-4.66% .. +6.02%] · haut q95 +8.6% · bas q05 -6.14%
   - 6h (n=160) : retour [-5.55% .. +6.71%] · haut q95 +8.6% · bas q05 -6.82%
   - session (n=160) : retour [-5.03% .. +6.26%] · haut q95 +8.6% · bas q05 -7.16%


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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 23.4  _(pas de tendance nette)_
- **MACD** : hist -0.143  _(bearish_recent)_
- **BB** : %B 0.68 · largeur 34.6%
- **ATR** : 7.01 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.0  _(neutre)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 47.0  _(transition)_
- **MA** : MA20 94.55 · MA50 85.71 · MA200 102.41  _(prix > MA20)_
- **Dist MA** : MA20 +6.1% · MA50 +17.0% · MA200 -2.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94820 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
