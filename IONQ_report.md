# IONQ

**Generated** : 2026-06-29T00:15:51.029241+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $49.31  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $49.31 (+2.9% vs entrée) · entrée $47.92 · stop $46.29 · T1 $49.47 · R/R 0.95  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.021 _(réel 5 s)_ (GBM -0.024) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.41% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $47.61–$48.23 (mid $47.92)
- Spot actuel : $49.31 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $46.29 (stop swing_plan-based (-9.59%))
- Targets : T1 $49.47 · R/R 0.95 | T2 $51.02 · R/R 1.9 | T3 $52.58 · R/R 2.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $46.29


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.038 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.063 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 11.2 | side 80.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.821% → cible +3.237% / stop −3.405%, p_fill 55%, n_eff≈22.1) : P(cible|rempli) **46%** · **EV/risk -0.021** (×p_fill ; si rempli -0.13% du capital)
  - **swing** (entrée dip −6.195% → cible +7.239% / stop −3.619%, p_fill 40%, n_eff≈15.8) : P(cible|rempli) **29%** · **EV/risk -0.085** (×p_fill ; si rempli -0.78% du capital)
  - **deep** (entrée dip −9.571% → cible +10.237% / stop −5.119%, p_fill 39%, n_eff≈13.5) : P(cible|rempli) **40%** · **EV/risk +0.054** (×p_fill ; si rempli +0.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→57% · +5.0%→31% · +8.0%→18%
- Range intraday médian 7.64% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.78%
- Profil de vol intra : ouverture 4.793% vs midi 1.604% vs clôture 1.688% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 75% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; momentum — autocorr 0.035)_ ; drift intra méd. -0.007% ; recovery-V 42%
- **σ réalisé intraday** 5.48% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 53% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 51.4771 (VA 50.7511–52.2939 ; dernier close 49.16)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 85% · **stop −4.75%** sous le fill (sous le bruit) · cible +3.44% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.33% · baisse 53% (gap-down >1% 38% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.32% (p90 −3.09%) · haut méd +0.93% · range méd 2.55%
- Excursion ouverture 15min (n=160) : bas méd −1.85% (p90 −3.97%) · haut méd +1.23% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −2.05% (p90 −5.32%) · haut méd +1.76% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.51% (p90 −6.02%) · haut méd +2.12% · range méd 5.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 49.16 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (133/159) · gap 48% · délai 0.0min · rebond 72% (94/133) (MFE +2.26%)
   - −1.0% : fill 30min 74% · séance 81% (126/159) · gap 38% · délai 0.0min · rebond 77% (93/126) (MFE +2.72%)
   - −1.5% : fill 30min 69% · séance 78% (120/159) · gap 31% · délai 0.0min · rebond 72% (84/120) (MFE +2.53%)
   - −2.0% : fill 30min 60% · séance 72% (113/159) · gap 19% · délai 0.3min · rebond 73% (80/113) (MFE +2.71%)
   - −3.0% : fill 30min 51% · séance 62% (92/159) · gap 12% · délai 5.3min · rebond 77% (69/92) (MFE +3.43%)
   - −4.0% : fill 30min 31% · séance 49% (74/159) · gap 6% · délai 17.6min · rebond 82% (57/74) (MFE +2.56%)
   - −5.0% : fill 30min 21% · séance 42% (65/159) · gap 3% · délai 29.0min · rebond 85% (56/65) (MFE +3.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.89%) → stop au-delà de −2.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.21% (p90 −3.67%) → stop au-delà de −2.67% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.33% (p90 −3.72%) → stop au-delà de −2.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1117 jambes) : jambe baissière méd −1.36% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 100% (70/70) · rebond 76% (52/70)
      · −2.0% : fill 92% (65/70) · rebond 79% (51/65)
      · −3.0% : fill 82% (56/70) · rebond 76% (44/56)
      · −4.0% : fill 64% (44/70) · rebond 81% (36/44)
      · −5.0% : fill 55% (38/70) · rebond 80% (32/38)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 81% (9/14)
      · −2.0% : fill 60% (13/17) · rebond 49% (7/13)
      · −3.0% : fill 45% (10/17) · rebond 52% (6/10)
      · −4.0% : fill 40% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/17) · rebond 91% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 58% (42/72) · rebond 77% (32/42)
      · −2.0% : fill 50% (35/72) · rebond 64% (22/35)
      · −3.0% : fill 40% (26/72) · rebond 85% (19/26)
      · −4.0% : fill 30% (23/72) · rebond 88% (18/23)
      · −5.0% : fill 25% (20/72) · rebond 97% (18/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 60% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 82% si début vert vs 24% si rouge (base 50% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **82%** · continue >prix actuel 55% ; creux résiduel méd -2.22% (q20 -3.62%) → **SL/trailing à −3.62%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.15% / q75 +3.37% → **scale +2.15% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **24%** (continue à baisser 49%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +2.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.21% .. +7.17%] · haut q95 +8.24% · bas q05 -6.17%
   - 60min (n=160) : retour [-5.31% .. +7.13%] · haut q95 +11.09% · bas q05 -6.81%
   - 2h (n=160) : retour [-6.64% .. +9.03%] · haut q95 +11.58% · bas q05 -7.65%
   - 4h (n=160) : retour [-7.7% .. +9.03%] · haut q95 +12.54% · bas q05 -8.67%
   - 6h (n=160) : retour [-7.7% .. +7.64%] · haut q95 +12.87% · bas q05 -10.15%
   - session (n=160) : retour [-7.59% .. +9.62%] · haut q95 +12.89% · bas q05 -10.15%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
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

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.7  _(momentum baissier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist -1.653  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 44.0%
- **ATR** : 5.44 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.291  _(distribution)_
- **Vol ratio** : 2.33  _(volume au-dessus de la moyenne)_
- **Choppiness** : 58.2  _(transition)_
- **MA** : MA20 59.68 · MA50 54.51 · MA200 49.58  _(prix < MA20)_
- **Dist MA** : MA20 -17.4% · MA50 -9.5% · MA200 -0.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91333 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
