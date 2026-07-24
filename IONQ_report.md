# IONQ

**Generated** : 2026-07-24T22:01:25.426858+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $32.84  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $32.84 (+2.1% vs entrée) · entrée $32.15 · stop $31.39 · T1 $32.85 · R/R 0.92  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.229 _(réel 5 s)_ (GBM 0.011) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.37% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -111 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $32.01–$32.29 (mid $32.15)
- Spot actuel : $32.84 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : $31.39 (stop swing_plan-based (-6.96%))
- Targets : T1 $32.85 · R/R 0.92 | T2 $33.56 · R/R 1.86 | T3 $34.26 · R/R 2.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $31.39


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 34 % | T3 29 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.5 | bear 55.4 | side 26.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.096% → cible +2.188% / stop −2.374%, p_fill 71%, n_eff≈28.2) : P(cible|rempli) **28%** · **EV/risk -0.229** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −4.627% → cible +4.892% / stop −2.446%, p_fill 72%, n_eff≈26.3) : P(cible|rempli) **24%** · **EV/risk -0.183** (×p_fill ; si rempli -0.62% du capital)
  - **deep** (entrée dip −7.148% → cible +6.918% / stop −3.459%, p_fill 64%, n_eff≈21.9) : P(cible|rempli) **14%** · **EV/risk -0.396** (×p_fill ; si rempli -2.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→62% · +5.0%→32% · +8.0%→18%
- Range intraday médian 7.83% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −2.98%
- Profil de vol intra : ouverture 5.11% vs midi 1.568% vs clôture 1.65% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; neutre — autocorr 0.008)_ ; drift intra méd. -1.249% ; recovery-V 29%
- **σ réalisé intraday** 4.701% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 69% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 35.6741 (VA 35.1089–35.8736 ; dernier close 34.69)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 81% · **stop −5.1%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 54% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.26% (p90 −2.94%) · haut méd +0.99% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.81% (p90 −4.28%) · haut méd +1.32% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.25%) · haut méd +1.73% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.39% (p90 −5.91%) · haut méd +1.99% · range méd 5.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 34.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 83% (132/159) · gap 47% · délai 0.0min · rebond 69% (91/132) (MFE +1.89%)
   - −1.0% : fill 30min 70% · séance 80% (126/159) · gap 39% · délai 0.0min · rebond 73% (92/126) (MFE +2.38%)
   - −1.5% : fill 30min 68% · séance 78% (121/159) · gap 32% · délai 0.0min · rebond 68% (83/121) (MFE +2.5%)
   - −2.0% : fill 30min 57% · séance 69% (111/159) · gap 20% · délai 0.4min · rebond 65% (74/111) (MFE +2.5%)
   - −3.0% : fill 30min 48% · séance 59% (92/159) · gap 8% · délai 5.9min · rebond 71% (66/92) (MFE +3.03%)
   - −4.0% : fill 30min 30% · séance 46% (74/159) · gap 4% · délai 15.5min · rebond 73% (54/74) (MFE +2.0%)
   - −5.0% : fill 30min 20% · séance 41% (65/159) · gap 2% · délai 31.1min · rebond 81% (55/65) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.9% (p90 −2.84%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.05% (p90 −3.73%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −3.2%) → stop au-delà de −2.51% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1123 jambes) : jambe baissière méd −1.34% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 100% (73/73) · rebond 74% (55/73)
      · −2.0% : fill 95% (69/73) · rebond 72% (52/69)
      · −3.0% : fill 81% (59/73) · rebond 71% (44/59)
      · −4.0% : fill 62% (45/73) · rebond 71% (34/45)
      · −5.0% : fill 55% (39/73) · rebond 74% (31/39)
   - **flat** (15 séances) :
      · −1.0% : fill 64% (12/15) · rebond 82% (8/12)
      · −2.0% : fill 48% (11/15) · rebond 46% (5/11)
      · −3.0% : fill 36% (8/15) · rebond 48% (4/8)
      · −4.0% : fill 34% (7/15) · rebond 67% (3/7)
      · −5.0% : fill 34% (7/15) · rebond 91% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 59% (41/71) · rebond 70% (29/41)
      · −2.0% : fill 42% (31/71) · rebond 51% (17/31)
      · −3.0% : fill 35% (25/71) · rebond 78% (18/25)
      · −4.0% : fill 29% (22/71) · rebond 78% (17/22)
      · −5.0% : fill 25% (19/71) · rebond 99% (18/19)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 49% si les 15 1res min sont vertes (79 cas) · 34% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 75% si début vert vs 16% si rouge (base 42% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **75%** · continue >prix actuel 51% ; creux résiduel méd -2.18% (q20 -4.21%) → **SL/trailing à −4.21%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.77% / q75 +2.88% → **scale +1.77% / runner +2.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +1.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +6.49%] · haut q95 +7.35% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.33% .. +5.57%] · haut q95 +8.44% · bas q05 -6.82%
   - 2h (n=160) : retour [-6.49% .. +7.91%] · haut q95 +9.12% · bas q05 -7.44%
   - 4h (n=160) : retour [-7.34% .. +7.41%] · haut q95 +10.27% · bas q05 -8.39%
   - 6h (n=160) : retour [-7.64% .. +7.55%] · haut q95 +10.83% · bas q05 -8.75%
   - session (n=160) : retour [-7.46% .. +8.52%] · haut q95 +10.83% · bas q05 -8.77%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 10% vs absente 2% (base 5%)
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 8.7  _(survente)_
- **ADX** : 40.2  _(tendance tres forte)_
- **MACD** : hist -0.575  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 68.2%
- **ATR** : 2.54 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.446  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 31.8  _(marche directionnel)_
- **MA** : MA20 42.04 · MA50 52.43 · MA200 47.35  _(prix < MA20)_
- **Dist MA** : MA20 -21.9% · MA50 -37.4% · MA200 -30.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88897 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
