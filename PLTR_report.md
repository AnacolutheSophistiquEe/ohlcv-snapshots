# PLTR

**Generated** : 2026-07-02T00:16:36.885147+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $125.73  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $125.73 (+5.4% vs entrée) · entrée $119.34 · stop $109.79 · T1 $121.89 · R/R 0.27  
> ↳ P(T1 av. stop) 35 % · EV/risk -0.037 · ¼-Kelly 0.043 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.83–$119.85 (mid $119.34)
- Spot actuel : $125.73 (+5.4% au-dessus de la zone — repli à attendre)
- Stop : $109.79 (stop swing_plan-based (-12.31%))
- Targets : T1 $121.89 · R/R 0.27 | T2 $124.43 · R/R 0.53 | T3 $126.98 · R/R 0.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $109.79


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : $-0.349 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 7 % | T3 5 %
- Kelly (position) : f* 0.174 | ¼-Kelly 0.043 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.4 | bear 9.9 | side 72.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→39% · +3.0%→20% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.86% (p90 6.99%) · excursion haute méd. +1.77% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.823% vs midi 0.74% vs clôture 0.803% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓1% ; spike-down 55% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.394% ; recovery-V 21%
- **σ réalisé intraday** 2.654% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 54% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 117.5329 (VA 116.6351–118.5304 ; dernier close 116.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 49% · **stop −2.89%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.23% · baisse 57% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.97%) · haut méd +0.88% · range méd 1.73%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.79%) · haut méd +1.1% · range méd 2.2%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.54%) · haut méd +1.26% · range méd 2.61%
- Excursion ouverture 60min (n=160) : bas méd −1.35% (p90 −3.89%) · haut méd +1.43% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 116.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (116/159) · gap 43% · délai 0.0min · rebond 54% (63/116) (MFE +1.07%)
   - −1.0% : fill 30min 58% · séance 70% (107/159) · gap 31% · délai 0.0min · rebond 61% (63/107) (MFE +1.32%)
   - −1.5% : fill 30min 49% · séance 61% (89/159) · gap 21% · délai 1.0min · rebond 64% (55/89) (MFE +1.37%)
   - −2.0% : fill 30min 41% · séance 52% (74/159) · gap 15% · délai 4.2min · rebond 61% (46/74) (MFE +1.43%)
   - −3.0% : fill 30min 19% · séance 35% (54/159) · gap 4% · délai 21.1min · rebond 45% (25/54) (MFE +0.85%)
   - −4.0% : fill 30min 13% · séance 25% (39/159) · gap 3% · délai 28.5min · rebond 41% (18/39) (MFE +0.83%)
   - −5.0% : fill 30min 10% · séance 18% (27/159) · gap 2% · délai 26.4min · rebond 49% (14/27) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.75%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.38%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.38%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=541 jambes) : jambe baissière méd −1.09% (p90 −2.72%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 93% (63/67) · rebond 64% (39/63)
      · −2.0% : fill 78% (52/67) · rebond 61% (35/52)
      · −3.0% : fill 55% (37/67) · rebond 38% (18/37)
      · −4.0% : fill 41% (27/67) · rebond 37% (12/27)
      · −5.0% : fill 34% (20/67) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (59 séances) :
      · −1.0% : fill 33% (18/59) · rebond 72% (10/18)
      · −2.0% : fill 15% (9/59) · rebond 41% (3/9)
      · −3.0% : fill 5% (6/59) · rebond 14% (1/6)
      · −4.0% : fill 3% (4/59) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/59) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (80 cas) · 31% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:31** → P(séance verte=clôture>ouverture) 88% si début vert vs 11% si rouge (base 47% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 149min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **88%** · continue >prix actuel 43% ; creux résiduel méd -0.82% (q20 -1.57%) → **SL/trailing à −1.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.84% / q75 +1.33% → **scale +0.84% / runner +1.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 52%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.39%** (au-delà de la MAE q10 -2.39%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.01% .. +2.48%] · haut q95 +3.07% · bas q05 -4.21%
   - 60min (n=160) : retour [-3.47% .. +2.83%] · haut q95 +3.44% · bas q05 -4.46%
   - 2h (n=160) : retour [-3.72% .. +3.29%] · haut q95 +4.0% · bas q05 -4.5%
   - 4h (n=160) : retour [-4.47% .. +3.55%] · haut q95 +4.56% · bas q05 -5.54%
   - 6h (n=160) : retour [-5.06% .. +3.87%] · haut q95 +4.66% · bas q05 -5.62%
   - session (n=160) : retour [-4.98% .. +3.79%] · haut q95 +4.57% · bas q05 -5.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 3.1% / strong 1.9%) · base = 8 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.84% / p90 1.43%) · ~3.0 replis/séance, durée méd 76.74 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 30.0 min, n=25)
   - −1.0% → **39%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−1.43%** (p90, défaut prudent ; serré/agressif −0.84%) ; extension open→close méd +3.81% (q75 +4.61% / q95 +7.65%), MFE méd +4.14% / q90 +8.89%
   - Échelle scale-out : +4.14% (33%) / +6.64% (33%) / +8.89% (34%)
- **DÉSARMER** : repli > **−1.43%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.89% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.67 · part idiosyncratique 0.33
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.0  _(neutre)_
- **ADX** : 21.7  _(pas de tendance nette)_
- **MACD** : hist -0.451  _(pas de croisement recent)_
- **BB** : %B 0.48 · largeur 31.9%
- **ATR** : 6.39 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.203  _(distribution)_
- **Vol ratio** : 1.35  _(volume normal)_
- **Choppiness** : 41.7  _(transition)_
- **MA** : MA20 126.62 · MA50 134.92 · MA200 158.12  _(prix < MA20)_
- **Dist MA** : MA20 -0.7% · MA50 -6.8% · MA200 -20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89157 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
