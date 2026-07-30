# IONQ

**Generated** : 2026-07-30T00:24:59.013791+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $31.99  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $31.99 (+1.5% vs entrée) · entrée $31.51 · stop $30.71 · T1 $32.23 · R/R 0.9  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.231 _(réel 5 s)_ (GBM -0.002) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.53% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 350 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $31.37–$31.66 (mid $31.51)
- Spot actuel : $31.99 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $30.71 (stop swing_plan-based (-5.78%))
- Targets : T1 $32.23 · R/R 0.9 | T2 $32.95 · R/R 1.8 | T3 $33.66 · R/R 2.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.71


## Edge, scénarios & sizing

- EV/risk : -0.002 | EV/share : $-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 32 % | T3 29 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 31.1 | bear 54.7 | side 14.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.494% → cible +2.275% / stop −2.534%, p_fill 72%, n_eff≈30.4) : P(cible|rempli) **31%** · **EV/risk -0.231** (×p_fill ; si rempli -0.82% du capital)
  - **swing** (entrée dip −3.284% → cible +5.086% / stop −2.581%, p_fill 72%, n_eff≈29.5) : P(cible|rempli) **24%** · **EV/risk -0.207** (×p_fill ; si rempli -0.74% du capital)
  - **deep** (entrée dip −5.076% → cible +7.193% / stop −3.597%, p_fill 83%, n_eff≈30.4) : P(cible|rempli) **23%** · **EV/risk -0.257** (×p_fill ; si rempli -1.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→65% · +3.0%→61% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.76% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −3.27%
- Profil de vol intra : ouverture 5.238% vs midi 1.578% vs clôture 1.648% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; neutre — autocorr 0.022)_ ; drift intra méd. -1.055% ; recovery-V 30%
- **σ réalisé intraday** 4.728% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 70% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 33.7378 (VA 33.4652–34.0102 ; dernier close 33.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 82% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.63% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 55% (gap-down >1% 40% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.27% (p90 −2.94%) · haut méd +1.07% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.82% (p90 −4.27%) · haut méd +1.33% · range méd 3.68%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.33%) · haut méd +1.73% · range méd 4.55%
- Excursion ouverture 60min (n=160) : bas méd −2.4% (p90 −5.97%) · haut méd +2.03% · range méd 5.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 33.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 83% (132/159) · gap 47% · délai 0.0min · rebond 66% (90/132) (MFE +1.89%)
   - −1.0% : fill 30min 71% · séance 80% (126/159) · gap 40% · délai 0.0min · rebond 73% (92/126) (MFE +2.36%)
   - −1.5% : fill 30min 68% · séance 78% (121/159) · gap 33% · délai 0.0min · rebond 65% (82/121) (MFE +2.46%)
   - −2.0% : fill 30min 59% · séance 70% (111/159) · gap 20% · délai 0.3min · rebond 65% (75/111) (MFE +2.36%)
   - −3.0% : fill 30min 48% · séance 60% (92/159) · gap 10% · délai 7.0min · rebond 71% (66/92) (MFE +2.78%)
   - −4.0% : fill 30min 32% · séance 46% (73/159) · gap 6% · délai 15.4min · rebond 71% (54/73) (MFE +2.0%)
   - −5.0% : fill 30min 20% · séance 40% (63/159) · gap 2% · délai 24.8min · rebond 82% (54/63) (MFE +2.63%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.78%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.04% (p90 −3.62%) → stop au-delà de −2.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.98%) → stop au-delà de −2.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1123 jambes) : jambe baissière méd −1.34% (p90 −3.33%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 100% (74/74) · rebond 72% (55/74)
      · −2.0% : fill 95% (70/74) · rebond 70% (52/70)
      · −3.0% : fill 82% (60/74) · rebond 69% (44/60)
      · −4.0% : fill 61% (45/74) · rebond 67% (33/45)
      · −5.0% : fill 55% (39/74) · rebond 76% (31/39)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (69 séances) :
      · −1.0% : fill 56% (39/69) · rebond 71% (28/39)
      · −2.0% : fill 40% (29/69) · rebond 52% (17/29)
      · −3.0% : fill 34% (23/69) · rebond 78% (17/23)
      · −4.0% : fill 27% (20/69) · rebond 79% (17/20)
      · −5.0% : fill 24% (17/69) · rebond 100% (17/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 53% si les 15 1res min sont vertes (79 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 76% si début vert vs 18% si rouge (base 43% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -2.29% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +2.8% → **scale +1.84% / runner +2.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **18%** (continue à baisser 55%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.38%** (au-delà de la MAE q10 -4.38%), cible rebond +2.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +6.77%] · haut q95 +7.85% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.19% .. +5.44%] · haut q95 +8.38% · bas q05 -6.75%
   - 2h (n=160) : retour [-6.43% .. +7.84%] · haut q95 +8.97% · bas q05 -7.35%
   - 4h (n=160) : retour [-7.26% .. +7.2%] · haut q95 +10.16% · bas q05 -8.35%
   - 6h (n=160) : retour [-7.54% .. +7.49%] · haut q95 +10.16% · bas q05 -8.64%
   - session (n=160) : retour [-7.4% .. +8.11%] · haut q95 +10.16% · bas q05 -8.69%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 21.3  _(survente)_
- **ADX** : 40.8  _(tendance tres forte)_
- **MACD** : hist -0.07  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 62.3%
- **ATR** : 2.66 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.441  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 38.1  _(marche directionnel)_
- **MA** : MA20 39.31 · MA50 51.17 · MA200 46.7  _(prix < MA20)_
- **Dist MA** : MA20 -18.6% · MA50 -37.5% · MA200 -31.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88896 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
