# MSTR

**Generated** : 2026-07-29T00:21:09.343277+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $96.16  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-30 — MSTR earnings (J-1 sess · earnings)  
> ↳ spot $96.16 (+1.6% vs entrée) · entrée $94.62 · stop $90.84 · T1 $96.91 · R/R 0.61  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.026 _(réel 5 s)_ (GBM -0.015) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 175 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $94.17–$95.08 (mid $94.62)
- Spot actuel : $96.16 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : $90.84 (stop swing_plan-based (-6.12%))
- Targets : T1 $96.91 · R/R 0.61 | T2 $99.19 · R/R 1.21 | T3 $101.48 · R/R 1.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $90.84


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : $-0.057 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 18 % | T3 16 %
- Kelly (position) : f* 0.076 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 73.7 | bear 9.9 | side 16.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 192.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.594% → cible +2.415% / stop −4.0%, p_fill 71%, n_eff≈32.2) : P(cible|rempli) **40%** · **EV/risk -0.026** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −3.515% → cible +5.4% / stop −2.7%, p_fill 47%, n_eff≈23.2) : P(cible|rempli) **28%** · **EV/risk -0.098** (×p_fill ; si rempli -0.56% du capital)
  - **deep** (entrée dip −5.429% → cible +7.636% / stop −3.818%, p_fill 51%, n_eff≈24.2) : P(cible|rempli) **28%** · **EV/risk -0.097** (×p_fill ; si rempli -0.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→74% · +2.0%→59% · +3.0%→40% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.52% (p90 9.85%) · excursion haute méd. +2.63% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.444% vs midi 1.233% vs clôture 1.331% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.248% ; recovery-V 34%
- **σ réalisé intraday** 3.923% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 63% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 97.156 (VA 96.644–98.308 ; dernier close 98.64)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 70% · **stop −5.12%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. -0.22% · baisse 54% (gap-down >1% 40% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.06%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −2.84%) · haut méd +1.05% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.37%) · haut méd +1.37% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.8% (p90 −4.15%) · haut méd +1.58% · range méd 3.87%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 98.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (125/159) · gap 46% · délai 0.0min · rebond 49% (61/125) (MFE +0.96%)
   - −1.0% : fill 30min 63% · séance 73% (119/159) · gap 40% · délai 0.0min · rebond 57% (68/119) (MFE +1.15%)
   - −1.5% : fill 30min 57% · séance 67% (110/159) · gap 32% · délai 0.0min · rebond 55% (63/110) (MFE +1.48%)
   - −2.0% : fill 30min 49% · séance 62% (99/159) · gap 26% · délai 0.1min · rebond 60% (62/99) (MFE +1.32%)
   - −3.0% : fill 30min 37% · séance 53% (77/159) · gap 17% · délai 3.7min · rebond 59% (46/77) (MFE +1.56%)
   - −4.0% : fill 30min 24% · séance 44% (64/159) · gap 6% · délai 16.8min · rebond 60% (38/64) (MFE +1.65%)
   - −5.0% : fill 30min 15% · séance 29% (45/159) · gap 5% · délai 27.4min · rebond 70% (32/45) (MFE +1.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.9% (p90 −2.28%) → stop au-delà de −1.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.09% (p90 −2.8%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.11% (p90 −2.77%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=963 jambes) : jambe baissière méd −1.17% (p90 −2.74%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 99% (74/75) · rebond 49% (37/74)
      · −2.0% : fill 92% (67/75) · rebond 57% (39/67)
      · −3.0% : fill 85% (59/75) · rebond 60% (35/59)
      · −4.0% : fill 71% (49/75) · rebond 63% (31/49)
      · −5.0% : fill 48% (36/75) · rebond 72% (26/36)
   - **flat** (16 séances) :
      · −1.0% : fill 90% (15/16) · rebond 87% (11/15)
      · −2.0% : fill 58% (11/16) · rebond 64% (7/11)
      · −3.0% : fill 44% (7/16) · rebond 56% (4/7)
      · −4.0% : fill 29% (6/16) · rebond 12% (2/6)
      · −5.0% : fill 22% (4/16) · rebond 16% (2/4)
   - **gap-up** (68 séances) :
      · −1.0% : fill 37% (30/68) · rebond 66% (20/30)
      · −2.0% : fill 25% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 17% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 15% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 7% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 53% si les 15 1res min sont vertes (75 cas) · 37% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 74% si début vert vs 14% si rouge (base 45% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **74%** · continue >prix actuel 59% ; creux résiduel méd -1.72% (q20 -3.05%) → **SL/trailing à −3.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +3.11% → **scale +2.01% / runner +3.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **14%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.19%** (au-delà de la MAE q10 -5.19%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.67% .. +3.94%] · haut q95 +4.53% · bas q05 -4.04%
   - 60min (n=160) : retour [-4.9% .. +3.51%] · haut q95 +5.31% · bas q05 -5.05%
   - 2h (n=160) : retour [-4.71% .. +5.56%] · haut q95 +6.37% · bas q05 -5.22%
   - 4h (n=160) : retour [-7.22% .. +7.53%] · haut q95 +8.74% · bas q05 -8.27%
   - 6h (n=160) : retour [-6.42% .. +6.75%] · haut q95 +9.4% · bas q05 -8.28%
   - session (n=160) : retour [-5.83% .. +6.13%] · haut q95 +9.4% · bas q05 -8.28%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **17%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 6%)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 52.9  _(neutre)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist 1.828  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 15.4%
- **ATR** : 5.58 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.031  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 62.9  _(marche en range (choppy))_
- **MA** : MA20 95.88 · MA50 117.17 · MA200 161.12  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 -17.9% · MA200 -40.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92208 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
