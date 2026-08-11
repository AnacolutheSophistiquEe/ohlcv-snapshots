# CEG

**Generated** : 2026-08-11T00:29:02.893041+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $270.43  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $270.43 (+4.2% vs entrée) · entrée $259.61 · stop $255.72 · T1 $262.86 · R/R 0.84  
> ↳ P(T1 av. stop) 65 % · EV/risk 0.503 · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $258.96–$260.26 (mid $259.61)
- Spot actuel : $270.43 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $255.72 (stop swing_plan-based (-12.0%))
- Targets : T1 $262.86 · R/R 0.84 | T2 $266.11 · R/R 1.67 | T3 $269.35 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $255.72


## Edge, scénarios & sizing

- EV/risk : -0.033 | EV/share : $-0.128 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 26 % | T3 8 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.2 | bear 6.9 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.4% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.52%
- Profil de vol intra : ouverture 2.507% vs midi 0.677% vs clôture 0.782% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.374% ; recovery-V 10%
- **σ réalisé intraday** 2.375% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 61% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 268.4662 (VA 267.2787–270.3662 ; dernier close 269.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 39% · rebond 60% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 38% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.92%) · haut méd +0.86% · range méd 1.71%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.26%) · haut méd +1.0% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.9%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −3.09%) · haut méd +1.29% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 269.98 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 68% (116/159) · gap 24% · délai 0.8min · rebond 45% (55/116) (MFE +0.91%)
   - −1.0% : fill 30min 45% · séance 61% (102/159) · gap 18% · délai 2.1min · rebond 49% (55/102) (MFE +0.97%)
   - −1.5% : fill 30min 35% · séance 44% (85/159) · gap 10% · délai 3.7min · rebond 49% (45/85) (MFE +0.97%)
   - −2.0% : fill 30min 26% · séance 39% (69/159) · gap 7% · délai 9.2min · rebond 60% (43/69) (MFE +1.08%)
   - −3.0% : fill 30min 10% · séance 24% (42/159) · gap 2% · délai 38.6min · rebond 42% (15/42) (MFE +0.95%)
   - −4.0% : fill 30min 5% · séance 13% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 7% (17/159) · gap 0% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.43%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.14%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.37%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=471 jambes) : jambe baissière méd −1.08% (p90 −2.64%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 96% (54/55) · rebond 49% (30/54)
      · −2.0% : fill 76% (42/55) · rebond 58% (27/42)
      · −3.0% : fill 53% (29/55) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/55) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/55) · rebond 77% (11/15)
   - **flat** (29 séances) :
      · −1.0% : fill 64% (17/29) · rebond 33% (5/17)
      · −2.0% : fill 33% (9/29) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/29) · rebond 21% (1/7)
      · −4.0% : fill 10% (4/29) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/29) · rebond 61% (1/2)
   - **gap-up** (75 séances) :
      · −1.0% : fill 39% (31/75) · rebond 56% (20/31)
      · −2.0% : fill 19% (18/75) · rebond 70% (13/18)
      · −3.0% : fill 7% (6/75) · rebond 62% (2/6)
      · −4.0% : fill 2% (3/75) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/75) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 66% si les 15 1res min sont vertes (89 cas) · 24% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 76% si début vert vs 12% si rouge (base 47% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=91) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.07% (q20 -2.23%) → **SL/trailing à −2.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +2.21% → **scale +1.15% / runner +2.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **12%** (continue à baisser 71%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.87%** (au-delà de la MAE q10 -2.87%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.11% .. +2.27%] · haut q95 +2.69% · bas q05 -3.59%
   - 60min (n=160) : retour [-3.83% .. +2.75%] · haut q95 +3.37% · bas q05 -4.7%
   - 2h (n=160) : retour [-3.97% .. +2.99%] · haut q95 +4.18% · bas q05 -5.08%
   - 4h (n=160) : retour [-4.11% .. +3.43%] · haut q95 +4.2% · bas q05 -5.26%
   - 6h (n=160) : retour [-4.77% .. +3.41%] · haut q95 +4.55% · bas q05 -5.26%
   - session (n=160) : retour [-4.34% .. +3.36%] · haut q95 +4.67% · bas q05 -5.94%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist 0.66  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 11.7%
- **ATR** : 10.82 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.227  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 70.1  _(marche en range (choppy))_
- **MA** : MA20 264.04 · MA50 260.6 · MA200 303.93  _(prix > MA20)_
- **Dist MA** : MA20 +2.4% · MA50 +3.8% · MA200 -11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86732 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
