# IONQ

**Generated** : 2026-07-10T00:26:57.890530+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $44.77  

> 🟡 **WAIT-FOR-DIP** — spot +0.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $44.77 (+0.6% vs entrée) · entrée $44.49 · stop $43.23 · T1 $45.58 · R/R 0.87  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk 0.045 _(réel 5 s)_ (GBM 0.093) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.82% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $44.27–$44.71 (mid $44.49)
- Spot actuel : $44.77 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $43.23 (stop swing_plan-based (-4.19%))
- Targets : T1 $45.58 · R/R 0.87 | T2 $46.67 · R/R 1.73 | T3 $47.77 · R/R 2.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $43.23


## Edge, scénarios & sizing

- EV/risk : 0.093 | EV/share : $0.116 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 34 % | T3 33 %
- Kelly (position) : f* 0.09 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.2 | bear 14.0 | side 78.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.631% → cible +2.457% / stop −2.817%, p_fill 86%, n_eff≈35.7) : P(cible|rempli) **58%** · **EV/risk +0.045** (×p_fill ; si rempli +0.15% du capital)
  - **swing** (entrée dip −1.391% → cible +5.493% / stop −2.839%, p_fill 92%, n_eff≈35.4) : P(cible|rempli) **40%** · **EV/risk +0.131** (×p_fill ; si rempli +0.41% du capital)
  - **deep** (entrée dip −2.149% → cible +7.769% / stop −3.884%, p_fill 88%, n_eff≈33.2) : P(cible|rempli) **35%** · **EV/risk +0.028** (×p_fill ; si rempli +0.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→69% · +3.0%→65% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.84% (p90 12.54%) · excursion haute méd. +3.86% / basse méd. −2.97%
- Profil de vol intra : ouverture 4.983% vs midi 1.606% vs clôture 1.681% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; momentum — autocorr 0.04)_ ; drift intra méd. -0.238% ; recovery-V 40%
- **σ réalisé intraday** 5.147% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 64% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 44.7612 (VA 44.1987–45.1987 ; dernier close 45.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 60% · rebond 77% · **stop −5.9%** sous le fill (sous le bruit) · cible +3.31% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.55% · baisse 56% (gap-down >1% 40% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.24% (p90 −2.97%) · haut méd +1.03% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −3.9%) · haut méd +1.35% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.85% (p90 −5.18%) · haut méd +2.02% · range méd 4.44%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −6.1%) · haut méd +2.66% · range méd 5.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 45.06 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (133/159) · gap 50% · délai 0.0min · rebond 72% (93/133) (MFE +2.32%)
   - −1.0% : fill 30min 72% · séance 80% (125/159) · gap 40% · délai 0.0min · rebond 77% (92/125) (MFE +2.76%)
   - −1.5% : fill 30min 69% · séance 78% (120/159) · gap 34% · délai 0.0min · rebond 74% (84/120) (MFE +2.77%)
   - −2.0% : fill 30min 59% · séance 71% (112/159) · gap 23% · délai 0.2min · rebond 74% (79/112) (MFE +2.82%)
   - −3.0% : fill 30min 48% · séance 60% (92/159) · gap 10% · délai 5.0min · rebond 77% (69/92) (MFE +3.31%)
   - −4.0% : fill 30min 29% · séance 46% (73/159) · gap 5% · délai 17.5min · rebond 76% (55/73) (MFE +2.38%)
   - −5.0% : fill 30min 20% · séance 39% (64/159) · gap 2% · délai 28.4min · rebond 82% (55/64) (MFE +3.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.89%) → stop au-delà de −2.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.43%) → stop au-delà de −2.55% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.11% (p90 −3.46%) → stop au-delà de −2.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1114 jambes) : jambe baissière méd −1.34% (p90 −3.3%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 100% (73/73) · rebond 76% (54/73)
      · −2.0% : fill 94% (69/73) · rebond 79% (54/69)
      · −3.0% : fill 82% (59/73) · rebond 76% (46/59)
      · −4.0% : fill 60% (45/73) · rebond 72% (35/45)
      · −5.0% : fill 52% (39/73) · rebond 76% (32/39)
   - **flat** (17 séances) :
      · −1.0% : fill 64% (13/17) · rebond 83% (9/13)
      · −2.0% : fill 48% (12/17) · rebond 48% (6/12)
      · −3.0% : fill 36% (9/17) · rebond 50% (5/9)
      · −4.0% : fill 33% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 33% (7/17) · rebond 91% (6/7)
   - **gap-up** (69 séances) :
      · −1.0% : fill 57% (39/69) · rebond 78% (29/39)
      · −2.0% : fill 45% (31/69) · rebond 64% (19/31)
      · −3.0% : fill 36% (24/69) · rebond 86% (18/24)
      · −4.0% : fill 28% (21/69) · rebond 89% (17/21)
      · −5.0% : fill 23% (18/69) · rebond 98% (17/18)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 57% si les 15 1res min sont vertes (80 cas) · 39% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 78% si début vert vs 22% si rouge (base 49% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -2.17% (q20 -4.23%) → **SL/trailing à −4.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +3.35% → **scale +1.87% / runner +3.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 51%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.28%** (au-delà de la MAE q10 -5.28%), cible rebond +2.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.07% .. +7.16%] · haut q95 +7.94% · bas q05 -5.86%
   - 60min (n=160) : retour [-5.47% .. +6.03%] · haut q95 +9.48% · bas q05 -7.1%
   - 2h (n=160) : retour [-6.59% .. +8.48%] · haut q95 +10.32% · bas q05 -7.53%
   - 4h (n=160) : retour [-7.65% .. +7.65%] · haut q95 +11.84% · bas q05 -8.46%
   - 6h (n=160) : retour [-7.5% .. +7.64%] · haut q95 +12.12% · bas q05 -9.01%
   - session (n=160) : retour [-7.34% .. +9.33%] · haut q95 +12.13% · bas q05 -8.88%


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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -1.255  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 36.6%
- **ATR** : 4.18 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.366  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 44.1  _(transition)_
- **MA** : MA20 53.12 · MA50 55.09 · MA200 49.19  _(prix < MA20)_
- **Dist MA** : MA20 -15.7% · MA50 -18.7% · MA200 -9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88812 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
