# MSTR

**Generated** : 2026-07-30T00:21:04.503965+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $93.33  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-30 — MSTR earnings (J-0 sess · earnings)  
> ↳ spot $93.33 (+2.0% vs entrée) · entrée $91.51 · stop $89.16 · T1 $96.22 · R/R 2.0  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.223 _(réel 5 s)_ (GBM -0.207) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 166 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $90.57–$92.45 (mid $91.51)
- Spot actuel : $93.33 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $89.16 (stop swing_plan-based (-4.47%))
- Targets : T1 $96.22 · R/R 2.0 | T2 $100.93 · R/R 4.01 | T3 $105.63 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.16


## Edge, scénarios & sizing

- EV/risk : -0.207 | EV/share : $-0.486 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 14 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 66.2 | bear 18.1 | side 15.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 93.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.885% → cible +2.301% / stop −4.0%, p_fill 84%, n_eff≈36.7) : P(cible|rempli) **51%** · **EV/risk +0.002** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −1.948% → cible +5.145% / stop −2.572%, p_fill 70%, n_eff≈31.3) : P(cible|rempli) **25%** · **EV/risk -0.223** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −3.012% → cible +7.276% / stop −3.638%, p_fill 82%, n_eff≈32.3) : P(cible|rempli) **39%** · **EV/risk +0.025** (×p_fill ; si rempli +0.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→74% · +2.0%→60% · +3.0%→41% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.56% (p90 9.85%) · excursion haute méd. +2.72% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.473% vs midi 1.235% vs clôture 1.328% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.101 ; neutre — autocorr -0.02)_ ; drift intra méd. -0.204% ; recovery-V 38%
- **σ réalisé intraday** 3.917% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 60% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 95.705 (VA 95.575–97.655 ; dernier close 96.13)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 72% · **stop −5.03%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 55% (gap-down >1% 41% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.06%) · haut méd +0.78% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −2.84%) · haut méd +1.07% · range méd 2.49%
- Excursion ouverture 30min (n=160) : bas méd −1.39% (p90 −3.34%) · haut méd +1.37% · range méd 3.21%
- Excursion ouverture 60min (n=160) : bas méd −1.85% (p90 −4.14%) · haut méd +1.61% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 96.13 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (125/159) · gap 48% · délai 0.0min · rebond 48% (60/125) (MFE +0.94%)
   - −1.0% : fill 30min 64% · séance 73% (119/159) · gap 41% · délai 0.0min · rebond 55% (67/119) (MFE +1.07%)
   - −1.5% : fill 30min 57% · séance 68% (110/159) · gap 34% · délai 0.0min · rebond 56% (63/110) (MFE +1.32%)
   - −2.0% : fill 30min 50% · séance 62% (99/159) · gap 27% · délai 0.0min · rebond 61% (63/99) (MFE +1.37%)
   - −3.0% : fill 30min 38% · séance 54% (77/159) · gap 18% · délai 2.0min · rebond 61% (47/77) (MFE +1.74%)
   - −4.0% : fill 30min 25% · séance 45% (64/159) · gap 6% · délai 14.6min · rebond 62% (39/64) (MFE +1.66%)
   - −5.0% : fill 30min 17% · séance 30% (46/159) · gap 4% · délai 22.6min · rebond 72% (33/46) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.28%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.79%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.16% (p90 −2.75%) → stop au-delà de −2.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=966 jambes) : jambe baissière méd −1.16% (p90 −2.72%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 99% (75/76) · rebond 47% (37/75)
      · −2.0% : fill 92% (68/76) · rebond 59% (40/68)
      · −3.0% : fill 86% (60/76) · rebond 62% (36/60)
      · −4.0% : fill 72% (50/76) · rebond 65% (32/50)
      · −5.0% : fill 50% (37/76) · rebond 74% (27/37)
   - **flat** (15 séances) :
      · −1.0% : fill 90% (14/15) · rebond 87% (10/14)
      · −2.0% : fill 58% (10/15) · rebond 65% (7/10)
      · −3.0% : fill 43% (6/15) · rebond 57% (4/6)
      · −4.0% : fill 28% (5/15) · rebond 13% (2/5)
      · −5.0% : fill 22% (4/15) · rebond 16% (2/4)
   - **gap-up** (68 séances) :
      · −1.0% : fill 37% (30/68) · rebond 66% (20/30)
      · −2.0% : fill 25% (21/68) · rebond 71% (16/21)
      · −3.0% : fill 17% (11/68) · rebond 56% (7/11)
      · −4.0% : fill 15% (9/68) · rebond 66% (5/9)
      · −5.0% : fill 7% (5/68) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 53% si les 15 1res min sont vertes (74 cas) · 39% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 76% si début vert vs 16% si rouge (base 46% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -1.52% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.07% / q75 +3.16% → **scale +2.07% / runner +3.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **16%** (continue à baisser 61%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.41%** (au-delà de la MAE q10 -5.41%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.65% .. +3.93%] · haut q95 +4.43% · bas q05 -4.02%
   - 60min (n=160) : retour [-4.9% .. +3.49%] · haut q95 +5.3% · bas q05 -5.04%
   - 2h (n=160) : retour [-4.69% .. +5.55%] · haut q95 +6.11% · bas q05 -5.19%
   - 4h (n=160) : retour [-7.16% .. +7.39%] · haut q95 +8.69% · bas q05 -8.26%
   - 6h (n=160) : retour [-6.33% .. +6.64%] · haut q95 +9.21% · bas q05 -8.25%
   - session (n=160) : retour [-5.81% .. +6.11%] · haut q95 +9.21% · bas q05 -8.25%


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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-0 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-0 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-30 — MSTR earnings (J-0 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 49.3  _(neutre)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 1.546  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 12.9%
- **ATR** : 5.78 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.051  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 64.3  _(marche en range (choppy))_
- **MA** : MA20 96.2 · MA50 115.48 · MA200 159.98  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -19.2% · MA200 -41.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91431 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
