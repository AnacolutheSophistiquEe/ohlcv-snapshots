# ENR

**Generated** : 2026-07-27T21:39:59.815977+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €148.38  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €148.38 (+14.2% vs entrée) · entrée €129.90 · stop €127.32 · T1 €135.05 · R/R 2.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.098 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €128.86–€130.93 (mid €129.90)
- Spot actuel : €148.38 (+14.2% au-dessus de la zone — repli à attendre)
- Stop : €127.32 (stop swing_plan-based (-14.2%))
- Targets : T1 €135.05 · R/R 2.0 | T2 €140.21 · R/R 4.0 | T3 €145.37 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.32


## Edge, scénarios & sizing

- EV/risk : 0.098 | EV/share : €0.253 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 19 % | T3 5 %
- Kelly (position) : f* 0.041 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.0 | bear 19.0 | side 72.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→46% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.89% (p90 6.09%) · excursion haute méd. +1.53% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.041% vs midi 0.926% vs clôture 1.154% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.174% ; recovery-V 19%
- **σ réalisé intraday** 2.653% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 75% / bas 66% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 152.4228 (VA 151.9052–153.3543 ; dernier close 150.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 71% · **stop −4.24%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.26% · baisse 42% (gap-down >1% 23% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.82%) · haut méd +0.45% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.34%) · haut méd +0.61% · range méd 1.91%
- Excursion ouverture 60min (n=160) : bas méd −0.93% (p90 −2.57%) · haut méd +0.7% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 150.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (117/159) · gap 31% · délai 0.2min · rebond 55% (62/117) (MFE +1.12%)
   - −1.0% : fill 30min 52% · séance 68% (107/159) · gap 23% · délai 1.2min · rebond 58% (64/107) (MFE +1.42%)
   - −1.5% : fill 30min 42% · séance 60% (92/159) · gap 20% · délai 6.7min · rebond 64% (60/92) (MFE +1.59%)
   - −2.0% : fill 30min 26% · séance 46% (68/159) · gap 14% · délai 12.7min · rebond 59% (41/68) (MFE +1.38%)
   - −3.0% : fill 30min 16% · séance 34% (50/159) · gap 5% · délai 91.5min · rebond 63% (35/50) (MFE +1.51%)
   - −4.0% : fill 30min 8% · séance 22% (37/159) · gap 3% · délai 237.8min · rebond 64% (26/37) (MFE +1.72%)
   - −5.0% : fill 30min 3% · séance 16% (22/159) · gap 1% · délai 218.3min · rebond 71% (15/22) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −2.06%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.7%) → stop au-delà de −0.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.14%) → stop au-delà de −0.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=494 jambes) : jambe baissière méd −1.03% (p90 −2.5%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 97% (50/51) · rebond 58% (29/50)
      · −2.0% : fill 76% (37/51) · rebond 62% (24/37)
      · −3.0% : fill 58% (30/51) · rebond 54% (20/30)
      · −4.0% : fill 42% (24/51) · rebond 60% (17/24)
      · −5.0% : fill 32% (16/51) · rebond 69% (11/16)
   - **flat** (28 séances) :
      · −1.0% : fill 67% (21/28) · rebond 74% (15/21)
      · −2.0% : fill 28% (9/28) · rebond 56% (4/9)
      · −3.0% : fill 14% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 12% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/28) · rebond 74% (1/2)
   - **gap-up** (80 séances) :
      · −1.0% : fill 46% (36/80) · rebond 51% (20/36)
      · −2.0% : fill 30% (22/80) · rebond 54% (13/22)
      · −3.0% : fill 21% (15/80) · rebond 77% (12/15)
      · −4.0% : fill 11% (9/80) · rebond 69% (7/9)
      · −5.0% : fill 6% (4/80) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 86% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 51% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **86%** · continue >prix actuel 68% ; creux résiduel méd -1.15% (q20 -2.12%) → **SL/trailing à −2.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.33% / q75 +3.32% → **scale +2.33% / runner +3.32%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 65%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.65%** (au-delà de la MAE q10 -4.65%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.17%] · haut q95 +2.61% · bas q05 -2.73%
   - 60min (n=160) : retour [-2.45% .. +2.3%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.61%] · haut q95 +3.0% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.08% .. +2.67%] · haut q95 +3.87% · bas q05 -4.26%
   - 6h (n=160) : retour [-3.6% .. +3.53%] · haut q95 +4.39% · bas q05 -4.52%
   - session (n=160) : retour [-4.97% .. +4.34%] · haut q95 +5.42% · bas q05 -6.15%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **30 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.3  _(momentum baissier)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -0.25  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 18.1%
- **ATR** : 6.89 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.013  _(neutre)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 63.5  _(marche en range (choppy))_
- **MA** : MA20 155.79 · MA50 159.87 · MA200 143.83  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -7.2% · MA200 +3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93149 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
