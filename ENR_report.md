# ENR

**Generated** : 2026-07-28T21:39:57.818529+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €137.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €137.90 (+9.2% vs entrée) · entrée €126.28 · stop €123.72 · T1 €131.40 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.073 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -86 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €125.25–€127.30 (mid €126.28)
- Spot actuel : €137.90 (+9.2% au-dessus de la zone — repli à attendre)
- Stop : €123.72 (stop swing_plan-based (-10.29%))
- Targets : T1 €131.40 · R/R 2.0 | T2 €136.53 · R/R 4.0 | T3 €141.65 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €123.72


## Edge, scénarios & sizing

- EV/risk : 0.073 | EV/share : €0.187 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 18 % | T3 5 %
- Kelly (position) : f* 0.027 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.1 | bear 23.4 | side 66.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.828% → cible +1.815% / stop −1.666%, p_fill 27%, n_eff≈10.4) : P(cible|rempli) **33%** · **EV/risk -0.001** (×p_fill ; si rempli -0.00% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→60% · +2.0%→45% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.89% (p90 6.09%) · excursion haute méd. +1.47% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.034% vs midi 0.922% vs clôture 1.158% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.008)_ ; drift intra méd. -0.319% ; recovery-V 18%
- **σ réalisé intraday** 2.644% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 67% / whipsaw 44%
- POC intraday (dernière séance, temps-au-prix) : 153.669 (VA 152.679–154.263 ; dernier close 148.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 71% · **stop −4.24%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 41% (gap-down >1% 22% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.56% (p90 −1.79%) · haut méd +0.45% · range méd 1.17%
- Excursion ouverture 15min (n=160) : bas méd −0.72% (p90 −2.21%) · haut méd +0.6% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.86% (p90 −2.33%) · haut méd +0.6% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.57%) · haut méd +0.67% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 148.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (117/159) · gap 30% · délai 0.2min · rebond 54% (62/117) (MFE +1.11%)
   - −1.0% : fill 30min 51% · séance 68% (107/159) · gap 22% · délai 1.2min · rebond 59% (64/107) (MFE +1.37%)
   - −1.5% : fill 30min 42% · séance 61% (92/159) · gap 20% · délai 10.5min · rebond 66% (60/92) (MFE +1.54%)
   - −2.0% : fill 30min 26% · séance 47% (69/159) · gap 14% · délai 13.1min · rebond 60% (42/69) (MFE +1.43%)
   - −3.0% : fill 30min 15% · séance 33% (50/159) · gap 4% · délai 91.5min · rebond 63% (35/50) (MFE +1.51%)
   - −4.0% : fill 30min 7% · séance 22% (37/159) · gap 3% · délai 237.8min · rebond 64% (26/37) (MFE +1.72%)
   - −5.0% : fill 30min 3% · séance 15% (22/159) · gap 1% · délai 218.3min · rebond 71% (15/22) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −2.06%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.7%) → stop au-delà de −0.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.14%) → stop au-delà de −0.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.04% (p90 −2.54%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 97% (49/50) · rebond 58% (28/49)
      · −2.0% : fill 76% (37/50) · rebond 62% (24/37)
      · −3.0% : fill 59% (30/50) · rebond 54% (20/30)
      · −4.0% : fill 42% (24/50) · rebond 60% (17/24)
      · −5.0% : fill 33% (16/50) · rebond 69% (11/16)
   - **flat** (28 séances) :
      · −1.0% : fill 67% (21/28) · rebond 74% (15/21)
      · −2.0% : fill 28% (9/28) · rebond 56% (4/9)
      · −3.0% : fill 14% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 12% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 8% (2/28) · rebond 74% (1/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 48% (37/81) · rebond 55% (21/37)
      · −2.0% : fill 33% (23/81) · rebond 59% (14/23)
      · −3.0% : fill 21% (15/81) · rebond 77% (12/15)
      · −4.0% : fill 10% (9/81) · rebond 69% (7/9)
      · −5.0% : fill 6% (4/81) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 86% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 50% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **86%** · continue >prix actuel 68% ; creux résiduel méd -1.15% (q20 -2.12%) → **SL/trailing à −2.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.33% / q75 +3.32% → **scale +2.33% / runner +3.32%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.59%** (au-delà de la MAE q10 -4.59%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.11%] · haut q95 +2.61% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.44% .. +2.27%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.61%] · haut q95 +2.98% · bas q05 -3.75%
   - 4h (n=160) : retour [-3.07% .. +2.67%] · haut q95 +3.86% · bas q05 -4.25%
   - 6h (n=160) : retour [-3.58% .. +3.52%] · haut q95 +4.36% · bas q05 -4.51%
   - session (n=160) : retour [-4.92% .. +4.33%] · haut q95 +5.4% · bas q05 -6.12%


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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 36.6  _(momentum baissier)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist -0.957  _(pas de croisement recent)_
- **BB** : %B -0.04 · largeur 19.9%
- **ATR** : 7.36 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.142  _(distribution)_
- **Vol ratio** : 2.06  _(volume au-dessus de la moyenne)_
- **Choppiness** : 55.2  _(transition)_
- **MA** : MA20 154.39 · MA50 159.27 · MA200 143.97  _(prix < MA20)_
- **Dist MA** : MA20 -10.7% · MA50 -13.4% · MA200 -4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94899 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
