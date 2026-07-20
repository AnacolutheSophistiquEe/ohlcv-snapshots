# IONQ

**Generated** : 2026-07-20T00:25:58.400880+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $34.78  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $34.78 (+0.4% vs entrée) · entrée $34.64 · stop $33.66 · T1 $35.48 · R/R 0.86  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.136 _(réel 5 s)_ (GBM 0.031) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.85% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -100 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $34.51–$34.78 (mid $34.64)
- Spot actuel : $34.78 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $33.66 (stop swing_plan-based (-8.34%))
- Targets : T1 $35.48 · R/R 0.86 | T2 $36.32 · R/R 1.71 | T3 $37.15 · R/R 2.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $33.66


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : $0.031 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 34 % | T3 32 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 10.9 | side 81.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.389% → cible +2.416% / stop −2.852%, p_fill 96%, n_eff≈38.7) : P(cible|rempli) **44%** · **EV/risk -0.136** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −0.784% → cible +15.232% / stop −7.616%, p_fill 96%, n_eff≈37.9) : P(cible|rempli) **9%** · **EV/risk -0.573** (×p_fill ; si rempli -4.55% du capital)
  - **deep** (entrée dip −1.138% → cible +21.852% / stop −10.926%, p_fill 94%, n_eff≈36.5) : P(cible|rempli) **11%** · **EV/risk -0.634** (×p_fill ; si rempli -7.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→65% · +3.0%→61% · +5.0%→34% · +8.0%→18%
- Range intraday médian 7.89% (p90 12.54%) · excursion haute méd. +3.78% / basse méd. −3.43%
- Profil de vol intra : ouverture 5.136% vs midi 1.604% vs clôture 1.654% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; momentum — autocorr 0.04)_ ; drift intra méd. -1.305% ; recovery-V 27%
- **σ réalisé intraday** 4.845% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 70% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 34.9684 (VA 34.3259–35.8679 ; dernier close 34.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 43% · rebond 81% · **stop −5.1%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.39% · baisse 55% (gap-down >1% 39% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.29% (p90 −2.94%) · haut méd +0.92% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.86% (p90 −4.3%) · haut méd +1.2% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.92% (p90 −5.26%) · haut méd +1.66% · range méd 4.49%
- Excursion ouverture 60min (n=160) : bas méd −2.64% (p90 −5.94%) · haut méd +1.91% · range méd 5.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 34.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (133/159) · gap 48% · délai 0.0min · rebond 67% (91/133) (MFE +2.09%)
   - −1.0% : fill 30min 73% · séance 81% (127/159) · gap 39% · délai 0.0min · rebond 72% (92/127) (MFE +2.38%)
   - −1.5% : fill 30min 70% · séance 79% (122/159) · gap 32% · délai 0.0min · rebond 68% (84/122) (MFE +2.5%)
   - −2.0% : fill 30min 61% · séance 71% (113/159) · gap 21% · délai 0.3min · rebond 67% (76/113) (MFE +2.59%)
   - −3.0% : fill 30min 51% · séance 62% (94/159) · gap 9% · délai 5.9min · rebond 72% (68/94) (MFE +3.03%)
   - −4.0% : fill 30min 32% · séance 49% (76/159) · gap 4% · délai 15.5min · rebond 73% (56/76) (MFE +2.03%)
   - −5.0% : fill 30min 21% · séance 43% (67/159) · gap 2% · délai 31.2min · rebond 81% (57/67) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.86%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.09% (p90 −3.84%) → stop au-delà de −2.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.11% (p90 −3.47%) → stop au-delà de −2.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1124 jambes) : jambe baissière méd −1.34% (p90 −3.4%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 100% (74/74) · rebond 72% (55/74)
      · −2.0% : fill 94% (70/74) · rebond 74% (53/70)
      · −3.0% : fill 84% (60/74) · rebond 71% (45/60)
      · −4.0% : fill 64% (46/74) · rebond 71% (35/46)
      · −5.0% : fill 57% (40/74) · rebond 74% (32/40)
   - **flat** (15 séances) :
      · −1.0% : fill 64% (12/15) · rebond 82% (8/12)
      · −2.0% : fill 48% (11/15) · rebond 46% (5/11)
      · −3.0% : fill 36% (8/15) · rebond 48% (4/8)
      · −4.0% : fill 34% (7/15) · rebond 67% (3/7)
      · −5.0% : fill 34% (7/15) · rebond 91% (6/7)
   - **gap-up** (70 séances) :
      · −1.0% : fill 60% (41/70) · rebond 68% (29/41)
      · −2.0% : fill 46% (32/70) · rebond 51% (18/32)
      · −3.0% : fill 39% (26/70) · rebond 78% (19/26)
      · −4.0% : fill 32% (23/70) · rebond 78% (18/23)
      · −5.0% : fill 28% (20/70) · rebond 99% (19/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 53% si les 15 1res min sont vertes (77 cas) · 32% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 78% si début vert vs 17% si rouge (base 43% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -2.18% (q20 -4.23%) → **SL/trailing à −4.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +3.2% → **scale +1.87% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **17%** (continue à baisser 56%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +6.85%] · haut q95 +7.62% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.38% .. +5.72%] · haut q95 +8.49% · bas q05 -6.85%
   - 2h (n=160) : retour [-6.53% .. +8.43%] · haut q95 +9.14% · bas q05 -7.48%
   - 4h (n=160) : retour [-7.46% .. +7.47%] · haut q95 +10.35% · bas q05 -8.41%
   - 6h (n=160) : retour [-7.69% .. +7.59%] · haut q95 +11.44% · bas q05 -8.8%
   - session (n=160) : retour [-7.49% .. +8.94%] · haut q95 +11.44% · bas q05 -8.82%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 11% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.89% / p90 2.79%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=39)
   - −1.0% → **74%** (reprise méd 20.0 min, n=24)
   - −1.5% → **59%** (reprise méd 38.13 min, n=12)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.79%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +7.79% (q75 +10.75% / q95 +18.2%), MFE méd +9.27% / q90 +19.18%
   - Échelle scale-out : +9.27% (33%) / +12.82% (33%) / +19.18% (34%)
- **DÉSARMER** : repli > **−2.79%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +19.18% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 20.3  _(survente)_
- **ADX** : 32.9  _(tendance etablie)_
- **MACD** : hist -1.441  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 62.7%
- **ATR** : 3.29 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.361  _(distribution)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 28.8  _(marche directionnel)_
- **MA** : MA20 47.32 · MA50 54.25 · MA200 48.22  _(prix < MA20)_
- **Dist MA** : MA20 -26.5% · MA50 -35.9% · MA200 -27.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88375 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
