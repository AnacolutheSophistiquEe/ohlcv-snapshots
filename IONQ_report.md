# IONQ

**Generated** : 2026-07-16T22:04:05.598481+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $35.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $35.10 (+0.5% vs entrée) · entrée $34.94 · stop $33.92 · T1 $35.78 · R/R 0.82  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk -0.064 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.91% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -98 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $34.77–$35.10 (mid $34.94)
- Spot actuel : $35.10 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $33.92 (stop swing_plan-based (-8.18%))
- Targets : T1 $35.78 · R/R 0.82 | T2 $36.62 · R/R 1.65 | T3 $37.46 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $33.92


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : $0.033 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 34 % | T3 32 %
- Kelly (position) : f* 0.048 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.9 | bear 13.2 | side 79.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.461% → cible +2.41% / stop −2.912%, p_fill 96%, n_eff≈38.5) : P(cible|rempli) **49%** · **EV/risk -0.064** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −1.022% → cible +14.464% / stop −7.232%, p_fill 95%, n_eff≈37.5) : P(cible|rempli) **10%** · **EV/risk -0.549** (×p_fill ; si rempli -4.18% du capital)
  - **deep** (entrée dip −1.517% → cible +21.208% / stop −10.604%, p_fill 92%, n_eff≈35.1) : P(cible|rempli) **11%** · **EV/risk -0.619** (×p_fill ; si rempli -7.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→64% · +3.0%→61% · +5.0%→34% · +8.0%→18%
- Range intraday médian 7.89% (p90 12.54%) · excursion haute méd. +3.78% / basse méd. −3.43%
- Profil de vol intra : ouverture 5.086% vs midi 1.593% vs clôture 1.653% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; momentum — autocorr 0.038)_ ; drift intra méd. -1.169% ; recovery-V 30%
- **σ réalisé intraday** 4.891% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 72% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 37.5479 (VA 37.0694–37.8669 ; dernier close 37.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 80% · **stop −5.15%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.3% · baisse 53% (gap-down >1% 39% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.29% (p90 −2.93%) · haut méd +0.92% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −4.27%) · haut méd +1.23% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −1.89% (p90 −5.27%) · haut méd +1.76% · range méd 4.49%
- Excursion ouverture 60min (n=160) : bas méd −2.51% (p90 −5.98%) · haut méd +2.16% · range méd 5.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 84% (133/159) · gap 48% · délai 0.0min · rebond 68% (91/133) (MFE +2.08%)
   - −1.0% : fill 30min 72% · séance 80% (127/159) · gap 39% · délai 0.0min · rebond 73% (92/127) (MFE +2.38%)
   - −1.5% : fill 30min 68% · séance 78% (122/159) · gap 33% · délai 0.0min · rebond 69% (84/122) (MFE +2.5%)
   - −2.0% : fill 30min 59% · séance 70% (113/159) · gap 21% · délai 0.2min · rebond 68% (77/113) (MFE +2.59%)
   - −3.0% : fill 30min 49% · séance 61% (93/159) · gap 9% · délai 6.0min · rebond 73% (68/93) (MFE +3.0%)
   - −4.0% : fill 30min 30% · séance 47% (75/159) · gap 5% · délai 18.5min · rebond 71% (55/75) (MFE +2.01%)
   - −5.0% : fill 30min 20% · séance 41% (66/159) · gap 2% · délai 31.2min · rebond 80% (56/66) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.0% (p90 −2.87%) → stop au-delà de −2.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.32%) → stop au-delà de −2.55% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.11% (p90 −3.46%) → stop au-delà de −2.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1120 jambes) : jambe baissière méd −1.34% (p90 −3.35%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 100% (73/73) · rebond 74% (54/73)
      · −2.0% : fill 94% (69/73) · rebond 76% (53/69)
      · −3.0% : fill 83% (59/73) · rebond 73% (45/59)
      · −4.0% : fill 62% (45/73) · rebond 68% (34/45)
      · −5.0% : fill 54% (39/73) · rebond 70% (31/39)
   - **flat** (15 séances) :
      · −1.0% : fill 64% (12/15) · rebond 82% (8/12)
      · −2.0% : fill 48% (11/15) · rebond 46% (5/11)
      · −3.0% : fill 36% (8/15) · rebond 48% (4/8)
      · −4.0% : fill 34% (7/15) · rebond 67% (3/7)
      · −5.0% : fill 34% (7/15) · rebond 91% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 60% (42/71) · rebond 68% (30/42)
      · −2.0% : fill 46% (33/71) · rebond 52% (19/33)
      · −3.0% : fill 39% (26/71) · rebond 78% (19/26)
      · −4.0% : fill 32% (23/71) · rebond 78% (18/23)
      · −5.0% : fill 28% (20/71) · rebond 99% (19/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 53% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 44% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -2.18% (q20 -4.23%) → **SL/trailing à −4.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +3.35% → **scale +1.87% / runner +3.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **18%** (continue à baisser 56%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.21% .. +7.08%] · haut q95 +7.72% · bas q05 -5.84%
   - 60min (n=160) : retour [-5.41% .. +5.87%] · haut q95 +8.52% · bas q05 -6.9%
   - 2h (n=160) : retour [-6.55% .. +8.45%] · haut q95 +9.29% · bas q05 -7.5%
   - 4h (n=160) : retour [-7.54% .. +7.54%] · haut q95 +11.49% · bas q05 -8.42%
   - 6h (n=160) : retour [-7.73% .. +7.63%] · haut q95 +11.71% · bas q05 -8.82%
   - session (n=160) : retour [-7.51% .. +9.33%] · haut q95 +11.71% · bas q05 -8.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.6)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.24% (p75 1.9% / p90 2.72%) · ~4.11 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=44)
   - −1.0% → **74%** (reprise méd 20.47 min, n=27)
   - −1.5% → **60%** (reprise méd 38.13 min, n=14)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.72%** (p90, défaut prudent ; serré/agressif −1.9%) ; extension open→close méd +7.82% (q75 +12.53% / q95 +18.2%), MFE méd +9.35% / q90 +18.66%
   - Échelle scale-out : +9.35% (33%) / +13.03% (33%) / +18.66% (34%)
- **DÉSARMER** : repli > **−2.72%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.66% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 19.6  _(survente)_
- **ADX** : 31.0  _(tendance etablie)_
- **MACD** : hist -1.497  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 57.7%
- **ATR** : 3.39 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.41  _(distribution)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 32.4  _(marche directionnel)_
- **MA** : MA20 48.31 · MA50 54.51 · MA200 48.37  _(prix < MA20)_
- **Dist MA** : MA20 -27.3% · MA50 -35.6% · MA200 -27.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88691 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
