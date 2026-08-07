# CEG

**Generated** : 2026-08-07T00:28:44.912174+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $261.10  

> 🟡 **WAIT-FOR-DIP** — spot +4.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $261.10 (+4.3% vs entrée) · entrée $250.32 · stop $246.57 · T1 $253.38 · R/R 0.82  
> ↳ P(T1 av. stop) 65 % · EV/risk 0.54 · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 131 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $249.71–$250.93 (mid $250.32)
- Spot actuel : $261.10 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : $246.57 (stop swing_plan-based (-12.38%))
- Targets : T1 $253.38 · R/R 0.82 | T2 $256.44 · R/R 1.63 | T3 $259.49 · R/R 2.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $246.57


## Edge, scénarios & sizing

- EV/risk : -0.035 | EV/share : $-0.133 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 27 % | T3 8 %
- Kelly (position) : f* 0.029 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.3 | bear 6.7 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→65% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.39% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.52%
- Profil de vol intra : ouverture 2.475% vs midi 0.67% vs clôture 0.759% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.247% ; recovery-V 11%
- **σ réalisé intraday** 2.218% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 62% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 265.8131 (VA 264.4694–266.0819 ; dernier close 264.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 60% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 40% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.88%) · haut méd +0.84% · range méd 1.67%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.21%) · haut méd +1.0% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.58%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.95%) · haut méd +1.3% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 264.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 69% (117/159) · gap 25% · délai 0.1min · rebond 43% (55/117) (MFE +0.9%)
   - −1.0% : fill 30min 47% · séance 61% (102/159) · gap 18% · délai 1.9min · rebond 50% (55/102) (MFE +1.04%)
   - −1.5% : fill 30min 36% · séance 46% (86/159) · gap 11% · délai 3.7min · rebond 49% (45/86) (MFE +0.97%)
   - −2.0% : fill 30min 27% · séance 41% (69/159) · gap 8% · délai 9.2min · rebond 60% (43/69) (MFE +1.08%)
   - −3.0% : fill 30min 11% · séance 24% (42/159) · gap 2% · délai 38.6min · rebond 42% (15/42) (MFE +0.95%)
   - −4.0% : fill 30min 6% · séance 13% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 7% (17/159) · gap 0% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −1.44%) → stop au-delà de −0.87% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.15%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.37%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 96% (54/55) · rebond 49% (30/54)
      · −2.0% : fill 76% (42/55) · rebond 58% (27/42)
      · −3.0% : fill 53% (29/55) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/55) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/55) · rebond 77% (11/15)
   - **flat** (31 séances) :
      · −1.0% : fill 64% (18/31) · rebond 33% (5/18)
      · −2.0% : fill 32% (9/31) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/31) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/31) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/31) · rebond 61% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 38% (30/73) · rebond 62% (20/30)
      · −2.0% : fill 21% (18/73) · rebond 70% (13/18)
      · −3.0% : fill 8% (6/73) · rebond 62% (2/6)
      · −4.0% : fill 2% (3/73) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/73) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (89 cas) · 25% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 75% si début vert vs 12% si rouge (base 47% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=91) : tient le vert **75%** · continue >prix actuel 51% ; creux résiduel méd -1.08% (q20 -2.27%) → **SL/trailing à −2.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.17% → **scale +1.08% / runner +2.17%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **12%** (continue à baisser 70%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.92%** (au-delà de la MAE q10 -2.92%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.28%] · haut q95 +2.7% · bas q05 -3.45%
   - 60min (n=160) : retour [-3.84% .. +2.77%] · haut q95 +3.37% · bas q05 -4.62%
   - 2h (n=160) : retour [-3.56% .. +3.0%] · haut q95 +4.18% · bas q05 -4.69%
   - 4h (n=160) : retour [-3.4% .. +3.44%] · haut q95 +4.29% · bas q05 -4.74%
   - 6h (n=160) : retour [-4.2% .. +3.43%] · haut q95 +4.58% · bas q05 -4.75%
   - session (n=160) : retour [-3.82% .. +3.44%] · haut q95 +4.67% · bas q05 -4.75%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.1  _(momentum haussier)_
- **ADX** : 13.3  _(pas de tendance nette)_
- **MACD** : hist 0.318  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 12.2%
- **ATR** : 10.78 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.186  _(distribution)_
- **Vol ratio** : 1.6  _(volume au-dessus de la moyenne)_
- **Choppiness** : 62.9  _(marche en range (choppy))_
- **MA** : MA20 262.47 · MA50 261.29 · MA200 304.85  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 -0.1% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86672 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
