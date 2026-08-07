# IONQ

**Generated** : 2026-08-07T00:26:06.444031+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $39.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $39.72 (+1.3% vs entrée) · entrée $39.22 · stop $36.49 · T1 $41.92 · R/R 0.99  
> ↳ P(T1 av. stop) 47 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM -0.109) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.05). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.270 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $38.72–$39.72 (mid $39.22)
- Spot actuel : $39.72 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $36.49 (stop swing_plan-based (-8.13%))
- Targets : T1 $41.92 · R/R 0.99 | T2 $44.62 · R/R 1.98 | T3 $47.32 · R/R 2.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $36.49


## Edge, scénarios & sizing

- EV/risk : -0.109 | EV/share : $-0.298 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 24 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 65.9 | bear 23.3 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 159.0 (= 4 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.57% → cible +3.08% / stop −2.072%, p_fill 83%, n_eff≈36.0) : P(cible|rempli) **27%** · **EV/risk -0.130** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −1.264% → cible +6.886% / stop −6.954%, p_fill 92%, n_eff≈38.4) : P(cible|rempli) **47%** · **EV/risk -0.079** (×p_fill ; si rempli -0.60% du capital)
  - **deep** (entrée dip −1.861% → cible +9.739% / stop −10.494%, p_fill 96%, n_eff≈37.3) : P(cible|rempli) **34%** · **EV/risk -0.281** (×p_fill ; si rempli -3.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→61% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.68% (p90 12.22%) · excursion haute méd. +3.69% / basse méd. −3.16%
- Profil de vol intra : ouverture 5.233% vs midi 1.507% vs clôture 1.699% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr 0.006)_ ; drift intra méd. -0.244% ; recovery-V 25%
- **σ réalisé intraday** 4.798% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 65% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 40.547 (VA 40.385–40.817 ; dernier close 39.92)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.37% · baisse 55% (gap-down >1% 39% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.17% (p90 −2.85%) · haut méd +1.2% · range méd 2.64%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.14%) · haut méd +1.37% · range méd 3.71%
- Excursion ouverture 30min (n=160) : bas méd −1.87% (p90 −5.25%) · haut méd +1.97% · range méd 4.52%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −5.91%) · haut méd +2.4% · range méd 5.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 81% (133/159) · gap 46% · délai 0.0min · rebond 67% (91/133) (MFE +1.89%)
   - −1.0% : fill 30min 69% · séance 77% (126/159) · gap 39% · délai 0.0min · rebond 75% (93/126) (MFE +2.35%)
   - −1.5% : fill 30min 66% · séance 75% (121/159) · gap 33% · délai 0.0min · rebond 68% (83/121) (MFE +2.52%)
   - −2.0% : fill 30min 58% · séance 68% (111/159) · gap 18% · délai 0.2min · rebond 68% (76/111) (MFE +2.53%)
   - −3.0% : fill 30min 47% · séance 57% (92/159) · gap 9% · délai 7.0min · rebond 73% (67/92) (MFE +2.75%)
   - −4.0% : fill 30min 30% · séance 45% (73/159) · gap 5% · délai 15.3min · rebond 74% (55/73) (MFE +2.38%)
   - −5.0% : fill 30min 18% · séance 37% (62/159) · gap 2% · délai 31.1min · rebond 83% (53/62) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.84%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.14%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −2.85%) → stop au-delà de −2.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1121 jambes) : jambe baissière méd −1.3% (p90 −3.18%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 100% (76/76) · rebond 75% (57/76)
      · −2.0% : fill 96% (72/76) · rebond 73% (54/72)
      · −3.0% : fill 81% (61/76) · rebond 71% (45/61)
      · −4.0% : fill 62% (46/76) · rebond 71% (35/46)
      · −5.0% : fill 52% (39/76) · rebond 77% (31/39)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (67 séances) :
      · −1.0% : fill 49% (37/67) · rebond 71% (27/37)
      · −2.0% : fill 34% (27/67) · rebond 52% (16/27)
      · −3.0% : fill 29% (22/67) · rebond 79% (17/22)
      · −4.0% : fill 24% (19/67) · rebond 79% (16/19)
      · −5.0% : fill 20% (16/67) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 54% si les 15 1res min sont vertes (80 cas) · 30% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 79% si début vert vs 16% si rouge (base 44% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -2.19% (q20 -3.47%) → **SL/trailing à −3.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.88% / q75 +2.85% → **scale +1.88% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **16%** (continue à baisser 59%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.19%** (au-delà de la MAE q10 -4.19%), cible rebond +1.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +7.17%] · haut q95 +8.14% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.11% .. +6.84%] · haut q95 +9.08% · bas q05 -6.61%
   - 2h (n=160) : retour [-6.34% .. +8.51%] · haut q95 +10.92% · bas q05 -7.21%
   - 4h (n=160) : retour [-7.23% .. +7.69%] · haut q95 +11.94% · bas q05 -8.21%
   - 6h (n=160) : retour [-7.46% .. +7.82%] · haut q95 +11.97% · bas q05 -8.44%
   - session (n=160) : retour [-7.27% .. +8.38%] · haut q95 +11.97% · bas q05 -8.44%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 2.08% / p90 3.34%) · ~3.45 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=44)
   - −1.0% → **72%** (reprise méd 49.72 min, n=27)
   - −1.5% → **56%** (reprise méd 81.24 min, n=14)
   - −2.0% → **51%** (reprise méd 175.66 min, n=10)
   - −3.0% → **62%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.34%** (p90, défaut prudent ; serré/agressif −2.08%) ; extension open→close méd +7.78% (q75 +8.69% / q95 +17.35%), MFE méd +9.24% / q90 +13.41%
   - Échelle scale-out : +9.24% (33%) / +12.23% (33%) / +13.41% (34%)
- **DÉSARMER** : repli > **−3.34%** depuis le plus-haut = décay → P(retournement) **44%** (préavis méd 168.41 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.41% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 75% du temps (retour médian dernière heure +0.28%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.6  _(momentum haussier)_
- **ADX** : 30.1  _(tendance etablie)_
- **MACD** : hist 1.362  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 32.7%
- **ATR** : 2.73 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.273  _(distribution)_
- **Vol ratio** : 1.24  _(volume normal)_
- **Choppiness** : 49.9  _(transition)_
- **MA** : MA20 36.7 · MA50 49.1 · MA200 45.71  _(prix > MA20)_
- **Dist MA** : MA20 +8.2% · MA50 -19.1% · MA200 -13.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92360 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
