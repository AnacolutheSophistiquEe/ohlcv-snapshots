# ENR

**Generated** : 2026-08-02T14:37:46.505393+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €148.14  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-04 — ENR earnings (J-1 sess · earnings)  
> ↳ spot €148.14 (+5.7% vs entrée) · entrée €140.15 · stop €137.75 · T1 €143.09 · R/R 1.22  
> ↳ P(T1 av. stop) 36 % · EV/risk -0.047 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.71% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €139.56–€140.74 (mid €140.15)
- Spot actuel : €148.14 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : €137.75 (stop swing_plan-based (-17.26%))
- Targets : T1 €143.09 · R/R 1.22 | T2 €146.03 · R/R 2.45 | T3 €148.96 · R/R 3.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €137.75


## Edge, scénarios & sizing

- EV/risk : -0.047 | EV/share : €-0.113 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 13 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.1 | bear 50.0 | side 40.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→60% · +2.0%→41% · +3.0%→26% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.02% (p90 6.67%) · excursion haute méd. +1.4% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.044% vs midi 0.919% vs clôture 1.159% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑2%/↓0% ; spike-down 58% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; neutre — autocorr -0.019)_ ; drift intra méd. -0.294% ; recovery-V 14%
- **σ réalisé intraday** 2.681% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 73% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 150.8537 (VA 149.6337–151.7688 ; dernier close 148.12)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 63% · **stop −4.13%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 42% (gap-down >1% 23% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.7%) · haut méd +0.47% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.7% (p90 −2.2%) · haut méd +0.64% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.26%) · haut méd +0.67% · range méd 1.85%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.57%) · haut méd +0.8% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 148.12 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (117/159) · gap 32% · délai 0.2min · rebond 55% (63/117) (MFE +1.12%)
   - −1.0% : fill 30min 51% · séance 69% (108/159) · gap 23% · délai 1.4min · rebond 63% (67/108) (MFE +1.44%)
   - −1.5% : fill 30min 39% · séance 62% (93/159) · gap 19% · délai 12.7min · rebond 66% (61/93) (MFE +1.6%)
   - −2.0% : fill 30min 24% · séance 47% (69/159) · gap 13% · délai 27.9min · rebond 60% (42/69) (MFE +1.43%)
   - −3.0% : fill 30min 14% · séance 32% (50/159) · gap 4% · délai 130.7min · rebond 60% (34/50) (MFE +1.41%)
   - −4.0% : fill 30min 7% · séance 22% (38/159) · gap 3% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 2% · séance 16% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.74%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.68%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.02%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=508 jambes) : jambe baissière méd −1.07% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 97% (51/52) · rebond 62% (30/51)
      · −2.0% : fill 74% (38/52) · rebond 58% (24/38)
      · −3.0% : fill 58% (31/52) · rebond 50% (20/31)
      · −4.0% : fill 43% (25/52) · rebond 53% (17/25)
      · −5.0% : fill 34% (17/52) · rebond 59% (11/17)
   - **flat** (28 séances) :
      · −1.0% : fill 71% (22/28) · rebond 78% (16/22)
      · −2.0% : fill 36% (10/28) · rebond 69% (5/10)
      · −3.0% : fill 13% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 11% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 7% (2/28) · rebond 74% (1/2)
   - **gap-up** (79 séances) :
      · −1.0% : fill 46% (35/79) · rebond 56% (21/35)
      · −2.0% : fill 31% (21/79) · rebond 60% (13/21)
      · −3.0% : fill 20% (14/79) · rebond 77% (11/14)
      · −4.0% : fill 10% (9/79) · rebond 69% (7/9)
      · −5.0% : fill 5% (4/79) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 77% si les 15 1res min sont vertes (77 cas) · 24% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 27% si rouge (base 48% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.0% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +2.71% → **scale +2.11% / runner +2.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **27%** (continue à baisser 52%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.49%** (au-delà de la MAE q10 -4.49%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.03%] · haut q95 +2.57% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.38% .. +2.16%] · haut q95 +2.7% · bas q05 -2.85%
   - 2h (n=160) : retour [-2.84% .. +2.46%] · haut q95 +2.91% · bas q05 -3.72%
   - 4h (n=160) : retour [-2.99% .. +2.66%] · haut q95 +3.85% · bas q05 -4.18%
   - 6h (n=160) : retour [-3.67% .. +4.02%] · haut q95 +4.89% · bas q05 -4.45%
   - session (n=160) : retour [-5.34% .. +4.47%] · haut q95 +5.91% · bas q05 -6.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 47.8  _(neutre)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -0.518  _(pas de croisement recent)_
- **BB** : %B 0.4 · largeur 18.9%
- **ATR** : 8.0 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.15  _(distribution)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 52.3  _(transition)_
- **MA** : MA20 151.0 · MA50 157.39 · MA200 144.52  _(prix < MA20)_
- **Dist MA** : MA20 -1.9% · MA50 -5.9% · MA200 +2.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94533 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
