# MSTR

**Generated** : 2026-06-30T21:47:58.749917+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $86.93  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $86.93 (+12.2% vs entrée) · entrée $77.46 · stop $71.26 · T1 $80.07 · R/R 0.42  
> ↳ P(T1 av. stop) 28 % · EV/risk -0.097 · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -34 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $76.93–$77.98 (mid $77.46)
- Spot actuel : $86.93 (+12.2% au-dessus de la zone — repli à attendre)
- Stop : $71.26 (stop swing_plan-based (-25.07%))
- Targets : T1 $80.07 · R/R 0.42 | T2 $82.68 · R/R 0.84 | T3 $85.29 · R/R 1.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $71.26


## Edge, scénarios & sizing

- EV/risk : -0.097 | EV/share : $-0.601 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.089 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.8 | bear 80.4 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→51% · +3.0%→32% · +5.0%→11% · +8.0%→5%
- Range intraday médian 5.22% (p90 9.27%) · excursion haute méd. +2.12% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.165% vs midi 1.201% vs clôture 1.238% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.01)_ ; drift intra méd. -1.466% ; recovery-V 30%
- **σ réalisé intraday** 4.077% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 78% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 93.0184 (VA 86.9441–94.1754 ; dernier close 92.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 69% · **stop −5.24%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 56% (gap-down >1% 40% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.08%) · haut méd +0.59% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.03%) · haut méd +0.82% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.81%) · haut méd +1.1% · range méd 3.05%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −4.96%) · haut méd +1.45% · range méd 3.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 92.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (127/159) · gap 47% · délai 0.0min · rebond 48% (63/127) (MFE +0.96%)
   - −1.0% : fill 30min 64% · séance 77% (122/159) · gap 40% · délai 0.0min · rebond 55% (68/122) (MFE +1.39%)
   - −1.5% : fill 30min 57% · séance 73% (114/159) · gap 29% · délai 0.0min · rebond 55% (67/114) (MFE +1.35%)
   - −2.0% : fill 30min 49% · séance 65% (102/159) · gap 24% · délai 1.3min · rebond 56% (64/102) (MFE +1.23%)
   - −3.0% : fill 30min 34% · séance 53% (78/159) · gap 13% · délai 9.4min · rebond 53% (47/78) (MFE +1.43%)
   - −4.0% : fill 30min 21% · séance 46% (64/159) · gap 5% · délai 38.8min · rebond 55% (39/64) (MFE +1.08%)
   - −5.0% : fill 30min 16% · séance 34% (49/159) · gap 3% · délai 58.2min · rebond 69% (35/49) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.75%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.06% (p90 −2.84%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.19% (p90 −3.14%) → stop au-delà de −2.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=971 jambes) : jambe baissière méd −1.21% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 48% (36/73)
      · −2.0% : fill 89% (66/74) · rebond 50% (38/66)
      · −3.0% : fill 79% (57/74) · rebond 55% (35/57)
      · −4.0% : fill 67% (47/74) · rebond 58% (31/47)
      · −5.0% : fill 54% (38/74) · rebond 71% (28/38)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (33/68) · rebond 62% (22/33)
      · −2.0% : fill 36% (23/68) · rebond 71% (17/23)
      · −3.0% : fill 24% (12/68) · rebond 55% (7/12)
      · −4.0% : fill 21% (10/68) · rebond 67% (6/10)
      · −5.0% : fill 11% (6/68) · rebond 93% (5/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 46% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 41% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **71%** · continue >prix actuel 50% ; creux résiduel méd -1.71% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +2.77% → **scale +1.72% / runner +2.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **19%** (continue à baisser 65%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.36%** (au-delà de la MAE q10 -5.36%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +3.28%] · haut q95 +4.0% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.11% .. +3.4%] · haut q95 +4.81% · bas q05 -5.57%
   - 2h (n=160) : retour [-4.82% .. +5.08%] · haut q95 +5.79% · bas q05 -5.64%
   - 4h (n=160) : retour [-7.81% .. +6.59%] · haut q95 +8.4% · bas q05 -8.38%
   - 6h (n=160) : retour [-7.19% .. +5.4%] · haut q95 +8.4% · bas q05 -8.65%
   - session (n=160) : retour [-6.2% .. +5.84%] · haut q95 +8.4% · bas q05 -8.65%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 3% (base 6%)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.7  _(momentum baissier)_
- **ADX** : 32.6  _(tendance etablie)_
- **MACD** : hist -2.131  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 58.3%
- **ATR** : 9.47 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.3  _(distribution)_
- **Vol ratio** : 1.25  _(volume normal)_
- **Choppiness** : 33.7  _(marche directionnel)_
- **MA** : MA20 112.69 · MA50 147.83 · MA200 183.59  _(prix < MA20)_
- **Dist MA** : MA20 -22.9% · MA50 -41.2% · MA200 -52.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89479 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
