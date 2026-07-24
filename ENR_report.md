# ENR

**Generated** : 2026-07-24T00:04:29.631104+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €149.94  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €149.94 (+6.7% vs entrée) · entrée €140.57 · stop €138.26 · T1 €143.28 · R/R 1.17  
> ↳ P(T1 av. stop) 41 % · EV/risk -0.003 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.64% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €140.03–€141.11 (mid €140.57)
- Spot actuel : €149.94 (+6.7% au-dessus de la zone — repli à attendre)
- Stop : €138.26 (stop swing_plan-based (-15.6%))
- Targets : T1 €143.28 · R/R 1.17 | T2 €145.98 · R/R 2.34 | T3 €148.69 · R/R 3.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €138.26


## Edge, scénarios & sizing

- EV/risk : -0.003 | EV/share : €-0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 61.0 | bear 31.9 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→48% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 4.01% (p90 6.09%) · excursion haute méd. +1.66% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.025% vs midi 0.937% vs clôture 1.149% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.139% ; recovery-V 21%
- **σ réalisé intraday** 2.679% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 62% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 156.9398 (VA 150.0517–161.2448 ; dernier close 152.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 71% · **stop −4.24%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.31% · baisse 41% (gap-down >1% 24% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.57% (p90 −1.83%) · haut méd +0.45% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.35%) · haut méd +0.61% · range méd 1.86%
- Excursion ouverture 60min (n=160) : bas méd −0.93% (p90 −2.59%) · haut méd +0.69% · range méd 2.0%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 152.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (117/159) · gap 32% · délai 0.2min · rebond 54% (61/117) (MFE +1.15%)
   - −1.0% : fill 30min 52% · séance 68% (107/159) · gap 24% · délai 1.2min · rebond 57% (63/107) (MFE +1.36%)
   - −1.5% : fill 30min 42% · séance 61% (92/159) · gap 21% · délai 3.8min · rebond 63% (59/92) (MFE +1.54%)
   - −2.0% : fill 30min 25% · séance 46% (68/159) · gap 14% · délai 11.5min · rebond 57% (40/68) (MFE +1.25%)
   - −3.0% : fill 30min 16% · séance 35% (51/159) · gap 5% · délai 94.0min · rebond 63% (36/51) (MFE +1.5%)
   - −4.0% : fill 30min 8% · séance 23% (38/159) · gap 3% · délai 240.4min · rebond 63% (26/38) (MFE +1.71%)
   - −5.0% : fill 30min 3% · séance 16% (22/159) · gap 1% · délai 218.3min · rebond 71% (15/22) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.65%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.72%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.14%) → stop au-delà de −0.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=498 jambes) : jambe baissière méd −1.02% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 97% (49/50) · rebond 56% (28/49)
      · −2.0% : fill 75% (36/50) · rebond 59% (23/36)
      · −3.0% : fill 62% (30/50) · rebond 54% (20/30)
      · −4.0% : fill 45% (24/50) · rebond 60% (17/24)
      · −5.0% : fill 34% (16/50) · rebond 69% (11/16)
   - **flat** (27 séances) :
      · −1.0% : fill 75% (21/27) · rebond 74% (15/21)
      · −2.0% : fill 32% (9/27) · rebond 56% (4/9)
      · −3.0% : fill 16% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 14% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/27) · rebond 74% (1/2)
   - **gap-up** (82 séances) :
      · −1.0% : fill 46% (37/82) · rebond 51% (20/37)
      · −2.0% : fill 30% (23/82) · rebond 54% (13/23)
      · −3.0% : fill 22% (16/82) · rebond 78% (13/16)
      · −4.0% : fill 11% (10/82) · rebond 67% (7/10)
      · −5.0% : fill 6% (4/82) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 86% si les 15 1res min sont vertes (75 cas) · 25% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 25% si rouge (base 51% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **86%** · continue >prix actuel 70% ; creux résiduel méd -1.12% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +3.33% → **scale +2.35% / runner +3.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **25%** (continue à baisser 64%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.73%** (au-delà de la MAE q10 -4.73%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.21%] · haut q95 +2.63% · bas q05 -2.78%
   - 60min (n=160) : retour [-2.47% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.61%] · haut q95 +3.02% · bas q05 -3.77%
   - 4h (n=160) : retour [-3.1% .. +2.67%] · haut q95 +3.88% · bas q05 -4.3%
   - 6h (n=160) : retour [-3.64% .. +3.57%] · haut q95 +4.45% · bas q05 -4.57%
   - session (n=160) : retour [-5.06% .. +4.34%] · haut q95 +5.43% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **30 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 20% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.7  _(momentum baissier)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist -0.219  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 17.3%
- **ATR** : 7.69 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.018  _(neutre)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 52.0  _(transition)_
- **MA** : MA20 156.32 · MA50 160.65 · MA200 143.39  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -6.7% · MA200 +4.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93989 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
