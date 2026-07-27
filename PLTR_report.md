# PLTR

**Generated** : 2026-07-27T21:59:52.057868+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $131.53  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $131.53 (+5.0% vs entrée) · entrée $125.24 · stop $122.11 · T1 $127.47 · R/R 0.71  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.03 · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $124.79–$125.69 (mid $125.24)
- Spot actuel : $131.53 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : $122.11 (stop swing_plan-based (-12.3%))
- Targets : T1 $127.47 · R/R 0.71 | T2 $129.70 · R/R 1.42 | T3 $131.93 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $122.11


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : $-0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 14 % | T3 6 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.9 | bear 10.9 | side 75.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 132.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→75% · +2.0%→46% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.94% (p90 7.17%) · excursion haute méd. +1.88% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.006% vs midi 0.738% vs clôture 0.859% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.004% ; recovery-V 31%
- **σ réalisé intraday** 2.743% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 47% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 123.6525 (VA 122.9775–123.8775 ; dernier close 122.93)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 56% · **stop −2.33%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 57% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.07%) · haut méd +0.92% · range méd 1.93%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −3.0%) · haut méd +1.06% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.5%) · haut méd +1.22% · range méd 2.83%
- Excursion ouverture 60min (n=160) : bas méd −1.38% (p90 −4.0%) · haut méd +1.38% · range méd 3.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.93 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (118/159) · gap 41% · délai 0.0min · rebond 52% (64/118) (MFE +1.07%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 30% · délai 0.0min · rebond 59% (62/108) (MFE +1.27%)
   - −1.5% : fill 30min 50% · séance 60% (92/159) · gap 23% · délai 0.2min · rebond 69% (58/92) (MFE +1.42%)
   - −2.0% : fill 30min 43% · séance 52% (77/159) · gap 15% · délai 1.5min · rebond 62% (47/77) (MFE +1.54%)
   - −3.0% : fill 30min 24% · séance 37% (55/159) · gap 8% · délai 7.2min · rebond 53% (25/55) (MFE +1.11%)
   - −4.0% : fill 30min 18% · séance 26% (40/159) · gap 4% · délai 15.5min · rebond 59% (20/40) (MFE +1.08%)
   - −5.0% : fill 30min 10% · séance 20% (28/159) · gap 2% · délai 26.1min · rebond 56% (14/28) (MFE +1.28%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.06%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.42%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=547 jambes) : jambe baissière méd −1.08% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 91% (66/71) · rebond 62% (40/66)
      · −2.0% : fill 77% (54/71) · rebond 63% (35/54)
      · −3.0% : fill 56% (38/71) · rebond 50% (18/38)
      · −4.0% : fill 43% (29/71) · rebond 56% (14/29)
      · −5.0% : fill 35% (22/71) · rebond 64% (12/22)
   - **flat** (29 séances) :
      · −1.0% : fill 79% (24/29) · rebond 34% (11/24)
      · −2.0% : fill 57% (13/29) · rebond 56% (7/13)
      · −3.0% : fill 47% (11/29) · rebond 56% (5/11)
      · −4.0% : fill 29% (8/29) · rebond 82% (5/8)
      · −5.0% : fill 15% (4/29) · rebond 14% (2/4)
   - **gap-up** (59 séances) :
      · −1.0% : fill 35% (18/59) · rebond 72% (11/18)
      · −2.0% : fill 19% (10/59) · rebond 69% (5/10)
      · −3.0% : fill 8% (6/59) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 68% si les 15 1res min sont vertes (79 cas) · 36% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 81% si début vert vs 23% si rouge (base 52% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.48% / q75 +2.52% → **scale +1.48% / runner +2.52%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **23%** (continue à baisser 50%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.34%** (au-delà de la MAE q10 -3.34%), cible rebond +1.36% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.71% .. +3.58%] · haut q95 +3.89% · bas q05 -4.06%
   - 60min (n=160) : retour [-3.65% .. +3.86%] · haut q95 +4.52% · bas q05 -4.4%
   - 2h (n=160) : retour [-4.18% .. +4.58%] · haut q95 +4.78% · bas q05 -4.58%
   - 4h (n=160) : retour [-4.53% .. +5.5%] · haut q95 +5.76% · bas q05 -5.58%
   - 6h (n=160) : retour [-5.12% .. +5.02%] · haut q95 +6.53% · bas q05 -5.81%
   - session (n=160) : retour [-4.99% .. +4.66%] · haut q95 +6.53% · bas q05 -5.86%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.8  _(neutre)_
- **ADX** : 12.0  _(pas de tendance nette)_
- **MACD** : hist 0.115  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 20.7%
- **ATR** : 6.88 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.175  _(accumulation)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 63.2  _(marche en range (choppy))_
- **MA** : MA20 128.33 · MA50 131.79 · MA200 154.34  _(prix > MA20)_
- **Dist MA** : MA20 +2.5% · MA50 -0.2% · MA200 -14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90119 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
