# CEG

**Generated** : 2026-06-30T21:55:54.411922+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $248.37  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $248.37 (+1.5% vs entrée) · entrée $244.62 · stop $241.12 · T1 $251.63 · R/R 2.0  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk -0.323 _(réel 5 s)_ (GBM 0.019) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $243.22–$246.02 (mid $244.62)
- Spot actuel : $248.37 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $241.12 (stop swing_plan-based (-2.92%))
- Targets : T1 $251.63 · R/R 2.0 | T2 $258.64 · R/R 4.01 | T3 $265.66 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $241.12


## Edge, scénarios & sizing

- EV/risk : 0.019 | EV/share : $0.067 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 22 % | T3 14 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 79.7 | bear 7.3 | side 13.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.69% → cible +1.282% / stop −1.5%, p_fill 78%, n_eff≈31.0) : P(cible|rempli) **45%** · **EV/risk -0.065** (×p_fill ; si rempli -0.13% du capital)
  - **swing** (entrée dip −1.508% → cible +2.866% / stop −1.433%, p_fill 54%, n_eff≈27.2) : P(cible|rempli) **15%** · **EV/risk -0.323** (×p_fill ; si rempli -0.86% du capital)
  - **deep** (entrée dip −2.33% → cible +4.054% / stop −2.027%, p_fill 61%, n_eff≈26.0) : P(cible|rempli) **18%** · **EV/risk -0.331** (×p_fill ; si rempli -1.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→35% · +3.0%→24% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.5%) · excursion haute méd. +1.49% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.53% vs midi 0.734% vs clôture 0.763% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.348% ; recovery-V 18%
- **σ réalisé intraday** 2.39% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 63% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 259.7144 (VA 258.9231–260.5056 ; dernier close 259.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 68% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 42% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.84%) · haut méd +0.76% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.28%) · haut méd +0.97% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.73%) · haut méd +1.08% · range méd 2.27%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.06%) · haut méd +1.3% · range méd 2.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 259.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 73% (119/159) · gap 27% · délai 0.0min · rebond 45% (59/119) (MFE +0.92%)
   - −1.0% : fill 30min 51% · séance 64% (104/159) · gap 23% · délai 1.9min · rebond 53% (58/104) (MFE +1.06%)
   - −1.5% : fill 30min 40% · séance 57% (91/159) · gap 12% · délai 3.8min · rebond 54% (51/91) (MFE +1.17%)
   - −2.0% : fill 30min 30% · séance 48% (71/159) · gap 10% · délai 10.5min · rebond 68% (47/71) (MFE +1.17%)
   - −3.0% : fill 30min 11% · séance 26% (43/159) · gap 4% · délai 50.6min · rebond 38% (18/43) (MFE +0.74%)
   - −4.0% : fill 30min 6% · séance 16% (28/159) · gap 2% · délai 37.5min · rebond 47% (14/28) (MFE +0.93%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 6.1min · rebond 61% (10/17) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.42%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.19%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=479 jambes) : jambe baissière méd −1.07% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 100% (53/53) · rebond 53% (33/53)
      · −2.0% : fill 85% (39/53) · rebond 69% (28/39)
      · −3.0% : fill 53% (24/53) · rebond 42% (10/24)
      · −4.0% : fill 35% (17/53) · rebond 46% (8/17)
      · −5.0% : fill 21% (13/53) · rebond 64% (9/13)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (69 séances) :
      · −1.0% : fill 39% (28/69) · rebond 63% (18/28)
      · −2.0% : fill 25% (18/69) · rebond 79% (13/18)
      · −3.0% : fill 8% (7/69) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/69) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/69) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (89 cas) · 20% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 12% si rouge (base 48% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 163min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **83%** · continue >prix actuel 40% ; creux résiduel méd -0.93% (q20 -1.94%) → **SL/trailing à −1.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.85% / q75 +1.7% → **scale +0.85% / runner +1.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **12%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.45%** (au-delà de la MAE q10 -2.45%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.01% .. +2.33%] · haut q95 +3.12% · bas q05 -3.75%
   - 60min (n=160) : retour [-3.44% .. +3.03%] · haut q95 +3.5% · bas q05 -4.13%
   - 2h (n=160) : retour [-3.74% .. +3.14%] · haut q95 +4.26% · bas q05 -4.7%
   - 4h (n=160) : retour [-3.79% .. +3.35%] · haut q95 +5.28% · bas q05 -5.0%
   - 6h (n=160) : retour [-4.33% .. +3.53%] · haut q95 +5.28% · bas q05 -5.01%
   - session (n=160) : retour [-4.28% .. +3.56%] · haut q95 +5.28% · bas q05 -5.0%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.1% / strong 2.5%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.29% / p90 1.8%) · ~2.0 replis/séance, durée méd 55.87 min. P(nouveau plus-haut après repli) :
   - −0.5% → **60%** (reprise méd 17.23 min, n=23)
   - −1.0% → **42%** (reprise méd 20.49 min, n=9)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.8%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +3.46% (q75 +4.43% / q95 +6.6%), MFE méd +3.74% / q90 +6.4%
   - Échelle scale-out : +3.74% (33%) / +5.32% (33%) / +6.4% (34%)
- **DÉSARMER** : repli > **−1.8%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.4% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 85% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.46 · part idiosyncratique 0.54
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.7  _(neutre)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 0.171  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 15.1%
- **ATR** : 9.69 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.169  _(distribution)_
- **Vol ratio** : 1.23  _(volume normal)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 261.51 · MA50 280.45 · MA200 316.97  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -11.4% · MA200 -21.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90448 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
