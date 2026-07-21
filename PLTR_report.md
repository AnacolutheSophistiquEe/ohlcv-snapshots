# PLTR

**Generated** : 2026-07-21T22:01:13.314644+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $132.66  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $132.66 (+12.2% vs entrée) · entrée $118.20 · stop $115.98 · T1 $122.65 · R/R 2.0  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.02 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $117.31–$119.09 (mid $118.20)
- Spot actuel : $132.66 (+12.2% au-dessus de la zone — repli à attendre)
- Stop : $115.98 (stop swing_plan-based (-12.58%))
- Targets : T1 $122.65 · R/R 2.0 | T2 $127.10 · R/R 4.01 | T3 $131.55 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.98


## Edge, scénarios & sizing

- EV/risk : -0.02 | EV/share : $-0.044 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 18 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.9 | bear 16.1 | side 61.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 265.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→49% · +3.0%→28% · +5.0%→8% · +8.0%→2%
- Range intraday médian 3.94% (p90 7.33%) · excursion haute méd. +1.95% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.974% vs midi 0.759% vs clôture 0.852% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 53% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr 0.029)_ ; drift intra méd. 0.564% ; recovery-V 41%
- **σ réalisé intraday** 2.795% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 47% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 135.6261 (VA 133.5426–136.4364 ; dernier close 134.86)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 62% · **stop −2.34%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 58% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.96% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.79%) · haut méd +1.18% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.1% (p90 −3.45%) · haut méd +1.32% · range méd 2.8%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.83%) · haut méd +1.52% · range méd 3.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 134.86 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (117/159) · gap 42% · délai 0.0min · rebond 55% (63/117) (MFE +1.14%)
   - −1.0% : fill 30min 57% · séance 66% (107/159) · gap 32% · délai 0.0min · rebond 60% (61/107) (MFE +1.31%)
   - −1.5% : fill 30min 48% · séance 59% (92/159) · gap 25% · délai 0.1min · rebond 66% (57/92) (MFE +1.57%)
   - −2.0% : fill 30min 40% · séance 51% (76/159) · gap 17% · délai 1.8min · rebond 62% (47/76) (MFE +1.43%)
   - −3.0% : fill 30min 24% · séance 36% (55/159) · gap 8% · délai 4.2min · rebond 53% (26/55) (MFE +1.13%)
   - −4.0% : fill 30min 17% · séance 26% (41/159) · gap 4% · délai 15.3min · rebond 57% (21/41) (MFE +1.31%)
   - −5.0% : fill 30min 11% · séance 19% (28/159) · gap 2% · délai 25.4min · rebond 62% (15/28) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.06%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.42%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.07% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 91% (67/72) · rebond 65% (41/67)
      · −2.0% : fill 76% (55/72) · rebond 61% (36/55)
      · −3.0% : fill 59% (40/72) · rebond 50% (20/40)
      · −4.0% : fill 45% (31/72) · rebond 56% (16/31)
      · −5.0% : fill 36% (23/72) · rebond 64% (13/23)
   - **flat** (28 séances) :
      · −1.0% : fill 76% (23/28) · rebond 40% (11/23)
      · −2.0% : fill 51% (12/28) · rebond 70% (7/12)
      · −3.0% : fill 40% (10/28) · rebond 75% (5/10)
      · −4.0% : fill 20% (7/28) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/28) · rebond 57% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/59) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/59) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 70% si les 15 1res min sont vertes (80 cas) · 40% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **42min** → P(séance verte=clôture>ouverture) 80% si début vert vs 27% si rouge (base 56% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **80%** · continue >prix actuel 55% ; creux résiduel méd -1.22% (q20 -2.38%) → **SL/trailing à −2.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.35% → **scale +1.21% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 46%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.25%** (au-delà de la MAE q10 -3.25%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.8% .. +3.66%] · haut q95 +3.94% · bas q05 -3.99%
   - 60min (n=160) : retour [-3.57% .. +3.87%] · haut q95 +4.61% · bas q05 -4.44%
   - 2h (n=160) : retour [-3.85% .. +4.75%] · haut q95 +4.8% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.36% .. +5.63%] · haut q95 +5.94% · bas q05 -5.11%
   - 6h (n=160) : retour [-4.95% .. +5.21%] · haut q95 +6.76% · bas q05 -5.55%
   - session (n=160) : retour [-4.69% .. +4.68%] · haut q95 +6.76% · bas q05 -5.55%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.2  _(surachat)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist 1.23  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 28.2%
- **ATR** : 7.04 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.046  _(neutre)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 61.3  _(transition)_
- **MA** : MA20 126.23 · MA50 132.41 · MA200 155.14  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +0.2% · MA200 -14.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87019 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
