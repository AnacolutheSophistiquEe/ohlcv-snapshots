# CEG

**Generated** : 2026-07-31T00:26:38.430986+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $263.56  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $263.56 (+3.7% vs entrée) · entrée $254.26 · stop $250.45 · T1 $257.28 · R/R 0.79  
> ↳ P(T1 av. stop) 57 % · EV/risk -0.017 · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $253.66–$254.87 (mid $254.26)
- Spot actuel : $263.56 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $250.45 (stop swing_plan-based (-8.29%))
- Targets : T1 $257.28 · R/R 0.79 | T2 $260.31 · R/R 1.59 | T3 $263.33 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $250.45


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : $-0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 30 % | T3 9 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.5 | bear 6.7 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→65% · +2.0%→39% · +3.0%→20% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.39% (p90 5.5%) · excursion haute méd. +1.47% / basse méd. −1.5%
- Profil de vol intra : ouverture 2.482% vs midi 0.72% vs clôture 0.742% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.085% ; recovery-V 6%
- **σ réalisé intraday** 2.217% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 258.5475 (VA 257.7835–260.0755 ; dernier close 257.92)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 62% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 44% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.86%) · haut méd +0.82% · range méd 1.64%
- Excursion ouverture 15min (n=160) : bas méd −0.65% (p90 −2.15%) · haut méd +0.99% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.82% (p90 −2.54%) · haut méd +1.04% · range méd 2.26%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.81%) · haut méd +1.29% · range méd 2.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257.92 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 70% (118/159) · gap 27% · délai 0.0min · rebond 44% (57/118) (MFE +0.91%)
   - −1.0% : fill 30min 49% · séance 61% (102/159) · gap 20% · délai 1.2min · rebond 52% (56/102) (MFE +1.07%)
   - −1.5% : fill 30min 38% · séance 48% (86/159) · gap 12% · délai 3.2min · rebond 51% (46/86) (MFE +1.04%)
   - −2.0% : fill 30min 28% · séance 42% (68/159) · gap 8% · délai 8.4min · rebond 62% (43/68) (MFE +1.15%)
   - −3.0% : fill 30min 12% · séance 25% (41/159) · gap 2% · délai 41.0min · rebond 38% (14/41) (MFE +0.79%)
   - −4.0% : fill 30min 6% · séance 15% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 1% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.55%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.98%) → stop au-delà de −0.66% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.37% (p90 −1.39%) → stop au-delà de −0.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=466 jambes) : jambe baissière méd −1.06% (p90 −2.58%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 96% (56/57) · rebond 49% (32/56)
      · −2.0% : fill 75% (42/57) · rebond 58% (27/42)
      · −3.0% : fill 52% (29/57) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/57) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/57) · rebond 77% (11/15)
   - **flat** (33 séances) :
      · −1.0% : fill 64% (19/33) · rebond 33% (5/19)
      · −2.0% : fill 32% (9/33) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/33) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/33) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/33) · rebond 61% (1/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 34% (27/69) · rebond 72% (19/27)
      · −2.0% : fill 21% (17/69) · rebond 84% (13/17)
      · −3.0% : fill 5% (5/69) · rebond 29% (1/5)
      · −4.0% : fill 2% (3/69) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/69) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (91 cas) · 23% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 73% si début vert vs 14% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=93) : tient le vert **73%** · continue >prix actuel 51% ; creux résiduel méd -1.08% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.04% → **scale +1.08% / runner +2.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **14%** (continue à baisser 70%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.68% .. +2.3%] · haut q95 +2.74% · bas q05 -3.26%
   - 60min (n=160) : retour [-2.93% .. +3.03%] · haut q95 +3.4% · bas q05 -4.04%
   - 2h (n=160) : retour [-3.64% .. +3.01%] · haut q95 +4.21% · bas q05 -4.53%
   - 4h (n=160) : retour [-3.55% .. +3.35%] · haut q95 +4.47% · bas q05 -4.61%
   - 6h (n=160) : retour [-4.24% .. +3.51%] · haut q95 +4.72% · bas q05 -4.86%
   - session (n=160) : retour [-3.97% .. +3.52%] · haut q95 +4.67% · bas q05 -4.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 16% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.18% (p75 1.36% / p90 1.68%) · ~1.0 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **71%** (reprise méd 32.71 min, n=20)
   - −1.0% → **67%** (reprise méd 175.01 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.68%** (p90, défaut prudent ; serré/agressif −1.36%) ; extension open→close méd +3.46% (q75 +4.38% / q95 +6.41%), MFE méd +3.74% / q90 +5.85%
   - Échelle scale-out : +3.74% (33%) / +5.06% (33%) / +5.85% (34%)
- **DÉSARMER** : repli > **−1.68%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.85% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-06 — CEG earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-06 — CEG earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 59.8  _(momentum haussier)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist 1.151  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 16.9%
- **ATR** : 9.3 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.01  _(neutre)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 50.1  _(transition)_
- **MA** : MA20 256.98 · MA50 263.16 · MA200 307.95  _(prix > MA20)_
- **Dist MA** : MA20 +2.6% · MA50 +0.2% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87021 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
