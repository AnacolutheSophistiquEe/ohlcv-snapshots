# MSTR

**Generated** : 2026-07-28T00:19:52.524368+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $98.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $98.65 (+2.2% vs entrée) · entrée $96.49 · stop $92.63 · T1 $99.14 · R/R 0.69  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.059 _(réel 5 s)_ (GBM -0.025) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 213 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $95.96–$97.02 (mid $96.49)
- Spot actuel : $98.65 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $92.63 (stop swing_plan-based (-7.73%))
- Targets : T1 $99.14 · R/R 0.69 | T2 $101.78 · R/R 1.37 | T3 $104.43 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $92.63


## Edge, scénarios & sizing

- EV/risk : -0.025 | EV/share : $-0.098 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.062 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 45.5 | bear 17.5 | side 37.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 197.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.187% → cible +2.741% / stop −4.0%, p_fill 57%, n_eff≈25.1) : P(cible|rempli) **32%** · **EV/risk -0.059** (×p_fill ; si rempli -0.41% du capital)
  - **swing** (entrée dip −4.813% → cible +6.129% / stop −3.065%, p_fill 45%, n_eff≈19.9) : P(cible|rempli) **19%** · **EV/risk -0.208** (×p_fill ; si rempli -1.41% du capital)
  - **deep** (entrée dip −7.438% → cible +8.669% / stop −4.334%, p_fill 51%, n_eff≈22.7) : P(cible|rempli) **51%** · **EV/risk +0.229** (×p_fill ; si rempli +1.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→74% · +2.0%→59% · +3.0%→40% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.48% (p90 9.85%) · excursion haute méd. +2.63% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.414% vs midi 1.236% vs clôture 1.334% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.103 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.466% ; recovery-V 34%
- **σ réalisé intraday** 3.948% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 66% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 92.7461 (VA 92.0654–93.3296 ; dernier close 91.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 70% · **stop −5.12%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 55% (gap-down >1% 41% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.07%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −2.84%) · haut méd +1.01% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.39% (p90 −3.43%) · haut méd +1.33% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.85% (p90 −4.19%) · haut méd +1.51% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 91.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (125/159) · gap 47% · délai 0.0min · rebond 49% (61/125) (MFE +0.96%)
   - −1.0% : fill 30min 64% · séance 74% (119/159) · gap 41% · délai 0.0min · rebond 57% (68/119) (MFE +1.15%)
   - −1.5% : fill 30min 58% · séance 68% (110/159) · gap 33% · délai 0.0min · rebond 55% (63/110) (MFE +1.48%)
   - −2.0% : fill 30min 50% · séance 63% (99/159) · gap 26% · délai 0.1min · rebond 60% (62/99) (MFE +1.32%)
   - −3.0% : fill 30min 38% · séance 54% (77/159) · gap 17% · délai 3.7min · rebond 59% (46/77) (MFE +1.56%)
   - −4.0% : fill 30min 24% · séance 45% (64/159) · gap 7% · délai 16.8min · rebond 60% (38/64) (MFE +1.65%)
   - −5.0% : fill 30min 16% · séance 30% (45/159) · gap 5% · délai 27.4min · rebond 70% (32/45) (MFE +1.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.28%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.12% (p90 −2.81%) → stop au-delà de −2.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.15% (p90 −2.79%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=965 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~12.0 jambes/séance
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
      · −1.0% : fill 38% (30/68) · rebond 66% (20/30)
      · −2.0% : fill 26% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 17% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 16% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 51% si les 15 1res min sont vertes (74 cas) · 37% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 73% si début vert vs 14% si rouge (base 44% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **73%** · continue >prix actuel 57% ; creux résiduel méd -1.75% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.13% → **scale +1.96% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **14%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.19%** (au-delà de la MAE q10 -5.19%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.72% .. +3.96%] · haut q95 +4.63% · bas q05 -4.07%
   - 60min (n=160) : retour [-4.9% .. +3.53%] · haut q95 +5.32% · bas q05 -5.1%
   - 2h (n=160) : retour [-4.73% .. +5.57%] · haut q95 +6.48% · bas q05 -5.27%
   - 4h (n=160) : retour [-7.33% .. +7.64%] · haut q95 +8.79% · bas q05 -8.28%
   - 6h (n=160) : retour [-6.58% .. +6.85%] · haut q95 +9.57% · bas q05 -8.32%
   - session (n=160) : retour [-5.86% .. +6.15%] · haut q95 +9.57% · bas q05 -8.32%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.4  _(neutre)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist 2.241  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 19.9%
- **ATR** : 5.63 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.008  _(neutre)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 64.0  _(marche en range (choppy))_
- **MA** : MA20 95.23 · MA50 120.71 · MA200 163.48  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 -18.3% · MA200 -39.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91907 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
