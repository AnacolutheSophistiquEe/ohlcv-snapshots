# PLTR

**Generated** : 2026-07-29T22:00:08.046671+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $123.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $123.00 (+3.5% vs entrée) · entrée $118.84 · stop $115.87 · T1 $121.11 · R/R 0.76  
> ↳ P(T1 av. stop) 47 % · EV/risk -0.021 · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.39–$119.30 (mid $118.84)
- Spot actuel : $123.00 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $115.87 (stop swing_plan-based (-9.41%))
- Targets : T1 $121.11 · R/R 0.76 | T2 $123.39 · R/R 1.53 | T3 $125.66 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.87


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : $-0.061 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 13 % | T3 6 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.9 | bear 10.5 | side 75.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.385% → cible +1.912% / stop −2.5%, p_fill 27%, n_eff≈10.4) : P(cible|rempli) **33%** · **EV/risk -0.044** (×p_fill ; si rempli -0.40% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→75% · +2.0%→46% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.96% (p90 7.17%) · excursion haute méd. +1.88% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.053% vs midi 0.735% vs clôture 0.861% _(ouverture ~4.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; momentum — autocorr 0.038)_ ; drift intra méd. 0.098% ; recovery-V 29%
- **σ réalisé intraday** 2.798% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 43% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 123.3032 (VA 122.8663–124.6142 ; dernier close 123.57)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 51% · **stop −3.07%** sous le fill (sous le bruit) · cible +1.01% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 57% (gap-down >1% 31% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.1%) · haut méd +0.94% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −3.02%) · haut méd +1.09% · range méd 2.38%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.69%) · haut méd +1.22% · range méd 2.84%
- Excursion ouverture 60min (n=160) : bas méd −1.38% (p90 −4.1%) · haut méd +1.37% · range méd 3.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 123.57 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (117/159) · gap 41% · délai 0.0min · rebond 51% (63/117) (MFE +1.04%)
   - −1.0% : fill 30min 59% · séance 68% (107/159) · gap 31% · délai 0.0min · rebond 58% (61/107) (MFE +1.25%)
   - −1.5% : fill 30min 50% · séance 60% (92/159) · gap 24% · délai 0.1min · rebond 67% (57/92) (MFE +1.38%)
   - −2.0% : fill 30min 43% · séance 52% (77/159) · gap 17% · délai 1.3min · rebond 60% (47/77) (MFE +1.43%)
   - −3.0% : fill 30min 25% · séance 37% (55/159) · gap 9% · délai 5.2min · rebond 50% (25/55) (MFE +0.99%)
   - −4.0% : fill 30min 19% · séance 26% (40/159) · gap 6% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 12% · séance 20% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.04%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.38%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=544 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 92% (66/71) · rebond 60% (39/66)
      · −2.0% : fill 78% (55/71) · rebond 60% (35/55)
      · −3.0% : fill 58% (39/71) · rebond 47% (18/39)
      · −4.0% : fill 45% (30/71) · rebond 51% (14/30)
      · −5.0% : fill 37% (23/71) · rebond 58% (12/23)
   - **flat** (28 séances) :
      · −1.0% : fill 78% (23/28) · rebond 34% (11/23)
      · −2.0% : fill 57% (12/28) · rebond 56% (7/12)
      · −3.0% : fill 46% (10/28) · rebond 57% (5/10)
      · −4.0% : fill 29% (7/28) · rebond 84% (5/7)
      · −5.0% : fill 15% (3/28) · rebond 9% (1/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 34% (18/60) · rebond 72% (11/18)
      · −2.0% : fill 18% (10/60) · rebond 69% (5/10)
      · −3.0% : fill 8% (6/60) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/60) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 69% si les 15 1res min sont vertes (78 cas) · 35% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 82% si début vert vs 22% si rouge (base 51% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **82%** · continue >prix actuel 60% ; creux résiduel méd -0.98% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.98% / q75 +2.55% → **scale +1.98% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **22%** (continue à baisser 48%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.33%** (au-delà de la MAE q10 -3.33%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +3.54%] · haut q95 +3.85% · bas q05 -4.34%
   - 60min (n=160) : retour [-3.94% .. +3.79%] · haut q95 +4.51% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.16% .. +4.54%] · haut q95 +4.78% · bas q05 -4.89%
   - 4h (n=160) : retour [-4.48% .. +5.31%] · haut q95 +5.71% · bas q05 -5.94%
   - 6h (n=160) : retour [-5.08% .. +4.94%] · haut q95 +6.23% · bas q05 -6.35%
   - session (n=160) : retour [-4.98% .. +4.64%] · haut q95 +6.23% · bas q05 -6.35%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 43.1  _(momentum baissier)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist -0.573  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 13.4%
- **ATR** : 6.86 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.144  _(accumulation)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 61.4  _(transition)_
- **MA** : MA20 129.54 · MA50 131.22 · MA200 153.43  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -6.3% · MA200 -19.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88832 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
