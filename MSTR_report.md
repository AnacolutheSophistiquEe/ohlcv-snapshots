# MSTR

**Generated** : 2026-07-01T21:48:42.906894+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $93.39  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $93.39 (+11.9% vs entrée) · entrée $83.46 · stop $76.78 · T1 $86.34 · R/R 0.43  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.092 · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $82.88–$84.04 (mid $83.46)
- Spot actuel : $93.39 (+11.9% au-dessus de la zone — repli à attendre)
- Stop : $76.78 (stop swing_plan-based (-24.45%))
- Targets : T1 $86.34 · R/R 0.43 | T2 $89.23 · R/R 0.86 | T3 $92.11 · R/R 1.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $76.78


## Edge, scénarios & sizing

- EV/risk : -0.092 | EV/share : $-0.615 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.087 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.2 | bear 79.5 | side 9.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→52% · +3.0%→32% · +5.0%→11% · +8.0%→5%
- Range intraday médian 5.22% (p90 9.27%) · excursion haute méd. +2.24% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.168% vs midi 1.206% vs clôture 1.244% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.008)_ ; drift intra méd. -1.358% ; recovery-V 34%
- **σ réalisé intraday** 4.125% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 79% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 85.3752 (VA 84.9013–86.4417 ; dernier close 86.93)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 65% · **stop −5.32%** sous le fill (sous le bruit) · cible +1.26% · R/R 0.24 (high win-rate)
- Gaps overnight (n=159) : méd. -0.33% · baisse 56% (gap-down >1% 41% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −2.07%) · haut méd +0.6% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −3.02%) · haut méd +0.84% · range méd 2.5%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.75%) · haut méd +1.09% · range méd 3.09%
- Excursion ouverture 60min (n=160) : bas méd −1.88% (p90 −4.96%) · haut méd +1.46% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 86.93 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (127/159) · gap 48% · délai 0.0min · rebond 47% (63/127) (MFE +0.95%)
   - −1.0% : fill 30min 65% · séance 77% (122/159) · gap 41% · délai 0.0min · rebond 54% (68/122) (MFE +1.34%)
   - −1.5% : fill 30min 58% · séance 73% (114/159) · gap 30% · délai 0.0min · rebond 54% (67/114) (MFE +1.19%)
   - −2.0% : fill 30min 50% · séance 65% (102/159) · gap 25% · délai 0.9min · rebond 54% (64/102) (MFE +1.16%)
   - −3.0% : fill 30min 35% · séance 54% (78/159) · gap 15% · délai 8.1min · rebond 51% (46/78) (MFE +1.38%)
   - −4.0% : fill 30min 22% · séance 46% (64/159) · gap 7% · délai 36.9min · rebond 53% (38/64) (MFE +1.04%)
   - −5.0% : fill 30min 18% · séance 35% (49/159) · gap 4% · délai 30.2min · rebond 65% (35/49) (MFE +1.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.73%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.09% (p90 −2.83%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.2% (p90 −3.14%) → stop au-delà de −2.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=970 jambes) : jambe baissière méd −1.21% (p90 −2.84%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 46% (36/73)
      · −2.0% : fill 89% (66/74) · rebond 48% (38/66)
      · −3.0% : fill 79% (57/74) · rebond 52% (34/57)
      · −4.0% : fill 68% (47/74) · rebond 54% (30/47)
      · −5.0% : fill 55% (38/74) · rebond 66% (28/38)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 46% si les 15 1res min sont vertes (71 cas) · 39% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 68% si début vert vs 22% si rouge (base 42% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 210min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **68%** · continue >prix actuel 49% ; creux résiduel méd -2.18% (q20 -4.39%) → **SL/trailing à −4.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.75% / q75 +3.02% → **scale +1.75% / runner +3.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.76%** (au-delà de la MAE q10 -5.76%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +3.25%] · haut q95 +4.0% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.1% .. +3.39%] · haut q95 +4.73% · bas q05 -5.55%
   - 2h (n=160) : retour [-4.81% .. +4.7%] · haut q95 +5.78% · bas q05 -5.62%
   - 4h (n=160) : retour [-7.74% .. +6.53%] · haut q95 +8.29% · bas q05 -8.35%
   - 6h (n=160) : retour [-7.19% .. +5.36%] · haut q95 +8.29% · bas q05 -8.6%
   - session (n=160) : retour [-6.16% .. +5.76%] · haut q95 +8.29% · bas q05 -8.6%


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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.4  _(momentum baissier)_
- **ADX** : 31.8  _(tendance etablie)_
- **MACD** : hist -1.261  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 57.9%
- **ATR** : 9.93 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.258  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 35.5  _(marche directionnel)_
- **MA** : MA20 110.56 · MA50 146.28 · MA200 182.4  _(prix < MA20)_
- **Dist MA** : MA20 -15.5% · MA50 -36.2% · MA200 -48.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89481 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
