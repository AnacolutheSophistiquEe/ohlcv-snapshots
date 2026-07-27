# IONQ

**Generated** : 2026-07-27T22:01:15.980476+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $35.92  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $35.92 (+1.3% vs entrée) · entrée $35.46 · stop $34.67 · T1 $36.30 · R/R 1.06  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.203 _(réel 5 s)_ (GBM -0.024) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.23% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $35.29–$35.63 (mid $35.46)
- Spot actuel : $35.92 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $34.67 (stop swing_plan-based (-5.38%))
- Targets : T1 $36.30 · R/R 1.06 | T2 $37.13 · R/R 2.11 | T3 $37.97 · R/R 3.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $34.67


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 28 % | T3 26 %
- Kelly (position) : f* 0.014 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 25.8 | bear 47.5 | side 26.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.285% → cible +2.359% / stop −2.234%, p_fill 84%, n_eff≈33.9) : P(cible|rempli) **33%** · **EV/risk -0.203** (×p_fill ; si rempli -0.54% du capital)
  - **swing** (entrée dip −2.817% → cible +5.274% / stop −2.637%, p_fill 75%, n_eff≈29.8) : P(cible|rempli) **26%** · **EV/risk -0.166** (×p_fill ; si rempli -0.59% du capital)
  - **deep** (entrée dip −4.353% → cible +7.459% / stop −3.729%, p_fill 86%, n_eff≈32.0) : P(cible|rempli) **28%** · **EV/risk -0.163** (×p_fill ; si rempli -0.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→65% · +3.0%→61% · +5.0%→30% · +8.0%→15%
- Range intraday médian 7.68% (p90 12.54%) · excursion haute méd. +3.69% / basse méd. −3.27%
- Profil de vol intra : ouverture 5.152% vs midi 1.556% vs clôture 1.643% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr 0.002)_ ; drift intra méd. -1.316% ; recovery-V 31%
- **σ réalisé intraday** 4.656% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 72% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 33.1019 (VA 32.9766–33.6029 ; dernier close 32.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 81% · **stop −5.09%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 55% (gap-down >1% 39% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.26% (p90 −2.94%) · haut méd +0.99% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.81% (p90 −4.28%) · haut méd +1.32% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.24%) · haut méd +1.73% · range méd 4.48%
- Excursion ouverture 60min (n=160) : bas méd −2.39% (p90 −5.9%) · haut méd +2.04% · range méd 5.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 84% (132/159) · gap 47% · délai 0.0min · rebond 68% (91/132) (MFE +1.89%)
   - −1.0% : fill 30min 71% · séance 81% (126/159) · gap 39% · délai 0.0min · rebond 74% (93/126) (MFE +2.38%)
   - −1.5% : fill 30min 69% · séance 79% (121/159) · gap 32% · délai 0.0min · rebond 67% (83/121) (MFE +2.51%)
   - −2.0% : fill 30min 59% · séance 70% (111/159) · gap 19% · délai 0.4min · rebond 67% (75/111) (MFE +2.52%)
   - −3.0% : fill 30min 48% · séance 60% (92/159) · gap 8% · délai 7.8min · rebond 73% (67/92) (MFE +2.79%)
   - −4.0% : fill 30min 31% · séance 46% (73/159) · gap 4% · délai 16.8min · rebond 74% (54/73) (MFE +2.17%)
   - −5.0% : fill 30min 19% · séance 39% (63/159) · gap 2% · délai 31.1min · rebond 81% (53/63) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −2.83%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.04% (p90 −3.68%) → stop au-delà de −2.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −3.09%) → stop au-delà de −2.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1123 jambes) : jambe baissière méd −1.34% (p90 −3.31%) · ~14.8 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 100% (73/73) · rebond 74% (55/73)
      · −2.0% : fill 95% (69/73) · rebond 73% (52/69)
      · −3.0% : fill 82% (59/73) · rebond 72% (44/59)
      · −4.0% : fill 60% (44/73) · rebond 71% (33/44)
      · −5.0% : fill 53% (38/73) · rebond 74% (30/38)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (70 séances) :
      · −1.0% : fill 59% (40/70) · rebond 71% (29/40)
      · −2.0% : fill 42% (30/70) · rebond 51% (17/30)
      · −3.0% : fill 35% (24/70) · rebond 79% (18/24)
      · −4.0% : fill 29% (21/70) · rebond 78% (17/21)
      · −5.0% : fill 25% (18/70) · rebond 99% (17/18)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 51% si les 15 1res min sont vertes (79 cas) · 33% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 75% si début vert vs 18% si rouge (base 42% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **75%** · continue >prix actuel 51% ; creux résiduel méd -2.18% (q20 -4.21%) → **SL/trailing à −4.21%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.77% / q75 +2.88% → **scale +1.77% / runner +2.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **18%** (continue à baisser 57%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.46%** (au-delà de la MAE q10 -4.46%), cible rebond +1.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.15% .. +6.24%] · haut q95 +7.03% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.28% .. +5.49%] · haut q95 +8.41% · bas q05 -6.79%
   - 2h (n=160) : retour [-6.46% .. +7.86%] · haut q95 +9.06% · bas q05 -7.41%
   - 4h (n=160) : retour [-7.28% .. +7.36%] · haut q95 +10.21% · bas q05 -8.38%
   - 6h (n=160) : retour [-7.6% .. +7.52%] · haut q95 +10.4% · bas q05 -8.72%
   - session (n=160) : retour [-7.44% .. +8.22%] · haut q95 +10.4% · bas q05 -8.74%


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
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 17.6  _(survente)_
- **ADX** : 39.2  _(tendance etablie)_
- **MACD** : hist -0.378  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 66.3%
- **ATR** : 2.64 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.399  _(distribution)_
- **Vol ratio** : 1.34  _(volume normal)_
- **Choppiness** : 35.0  _(marche directionnel)_
- **MA** : MA20 42.19 · MA50 52.49 · MA200 47.36  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -31.6% · MA200 -24.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89026 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
