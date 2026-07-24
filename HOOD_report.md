# HOOD

**Generated** : 2026-07-24T00:28:41.210560+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $101.58  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot $101.58 (+2.5% vs entrée) · entrée $99.06 · stop $96.41 · T1 $104.37 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.01 _(réel 5 s)_ (GBM -0.07) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $98.00–$100.12 (mid $99.06)
- Spot actuel : $101.58 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : $96.41 (stop swing_plan-based (-5.09%))
- Targets : T1 $104.37 · R/R 2.0 | T2 $109.67 · R/R 4.0 | T3 $114.98 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $96.41


## Edge, scénarios & sizing

- EV/risk : -0.07 | EV/share : $-0.185 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 14 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 45.1 | bear 38.2 | side 16.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 102.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.124% → cible +2.395% / stop −3.0%, p_fill 72%, n_eff≈30.9) : P(cible|rempli) **35%** · **EV/risk +0.005** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −2.479% → cible +5.355% / stop −2.677%, p_fill 58%, n_eff≈24.3) : P(cible|rempli) **35%** · **EV/risk -0.010** (×p_fill ; si rempli -0.04% du capital)
  - **deep** (entrée dip −3.829% → cible +7.573% / stop −3.786%, p_fill 46%, n_eff≈23.3) : P(cible|rempli) **47%** · **EV/risk +0.172** (×p_fill ; si rempli +1.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→56% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.08% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.602% vs midi 1.063% vs clôture 1.057% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 66% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.004)_ ; drift intra méd. 0.246% ; recovery-V 34%
- **σ réalisé intraday** 3.8% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 43% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 105.7463 (VA 105.0588–106.0588 ; dernier close 104.49)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 80% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 35% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −2.1%) · haut méd +1.0% · range méd 2.1%
- Excursion ouverture 15min (n=160) : bas méd −1.12% (p90 −3.16%) · haut méd +1.16% · range méd 2.83%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.84%) · haut méd +1.46% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −3.89%) · haut méd +1.7% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 104.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (122/159) · gap 42% · délai 0.0min · rebond 56% (61/122) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 67% (108/159) · gap 35% · délai 0.0min · rebond 62% (62/108) (MFE +1.46%)
   - −1.5% : fill 30min 50% · séance 60% (99/159) · gap 24% · délai 0.1min · rebond 55% (54/99) (MFE +1.54%)
   - −2.0% : fill 30min 41% · séance 52% (88/159) · gap 14% · délai 0.5min · rebond 66% (54/88) (MFE +1.35%)
   - −3.0% : fill 30min 30% · séance 40% (66/159) · gap 8% · délai 9.8min · rebond 73% (45/66) (MFE +1.94%)
   - −4.0% : fill 30min 18% · séance 31% (50/159) · gap 5% · délai 12.1min · rebond 80% (33/50) (MFE +2.33%)
   - −5.0% : fill 30min 11% · séance 20% (31/159) · gap 3% · délai 29.8min · rebond 80% (24/31) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −2.59%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −2.52%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.56%) → stop au-delà de −1.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=758 jambes) : jambe baissière méd −1.15% (p90 −2.8%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 96% (67/70) · rebond 58% (36/67)
      · −2.0% : fill 79% (56/70) · rebond 62% (33/56)
      · −3.0% : fill 65% (45/70) · rebond 70% (30/45)
      · −4.0% : fill 52% (36/70) · rebond 83% (26/36)
      · −5.0% : fill 37% (25/70) · rebond 77% (19/25)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 37% (25/68) · rebond 65% (15/25)
      · −2.0% : fill 24% (20/68) · rebond 85% (14/20)
      · −3.0% : fill 20% (15/68) · rebond 96% (13/15)
      · −4.0% : fill 13% (9/68) · rebond 87% (6/9)
      · −5.0% : fill 7% (3/68) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 67% si les 15 1res min sont vertes (71 cas) · 36% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 75% si début vert vs 27% si rouge (base 50% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **75%** · continue >prix actuel 55% ; creux résiduel méd -1.73% (q20 -3.55%) → **SL/trailing à −3.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +3.4% → **scale +1.65% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **27%** (continue à baisser 46%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.87%** (au-delà de la MAE q10 -3.87%), cible rebond +2.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.64% .. +4.36%] · haut q95 +4.94% · bas q05 -4.74%
   - 60min (n=160) : retour [-3.65% .. +4.6%] · haut q95 +6.25% · bas q05 -4.92%
   - 2h (n=160) : retour [-4.39% .. +5.98%] · haut q95 +7.57% · bas q05 -5.59%
   - 4h (n=160) : retour [-5.05% .. +6.16%] · haut q95 +8.35% · bas q05 -6.24%
   - 6h (n=160) : retour [-5.7% .. +6.72%] · haut q95 +8.35% · bas q05 -7.24%
   - session (n=160) : retour [-5.63% .. +6.31%] · haut q95 +8.68% · bas q05 -7.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 20% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.12%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=47)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.12%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.08% (q75 +9.69% / q95 +13.38%), MFE méd +6.77% / q90 +14.84%
   - Échelle scale-out : +6.77% (33%) / +11.24% (33%) / +14.84% (34%)
- **DÉSARMER** : repli > **−2.12%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.84% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.0  _(momentum baissier)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist -1.931  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 25.8%
- **ATR** : 6.32 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.018  _(neutre)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 51.3  _(transition)_
- **MA** : MA20 107.16 · MA50 94.99 · MA200 100.92  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 +6.9% · MA200 +0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91276 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
