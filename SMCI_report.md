# SMCI

**Generated** : 2026-07-22T21:58:56.268400+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $30.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $30.56 (+4.4% vs entrée) · entrée $29.28 · stop $28.13 · T1 $31.58 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.038 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.93% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $29.09–$29.47 (mid $29.28)
- Spot actuel : $30.56 (+4.4% au-dessus de la zone — repli à attendre)
- Stop : $28.13 (stop swing_plan-based (-12.54%))
- Targets : T1 $31.58 · R/R 2.0 | T2 $31.86 · R/R 2.24 | T3 $32.15 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $28.13


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : $0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.133 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.4 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 275.0 (= 9 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.195% → cible +7.859% / stop −3.929%, p_fill 33%, n_eff≈14.2) : P(cible|rempli) **4%** · **EV/risk -0.038** (×p_fill ; si rempli -0.45% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→64% · +3.0%→45% · +5.0%→26% · +8.0%→11%
- Range intraday médian 6.13% (p90 9.97%) · excursion haute méd. +2.57% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.791% vs midi 1.185% vs clôture 1.522% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. -0.524% ; recovery-V 21%
- **σ réalisé intraday** 3.933% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 67% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 25.315 (VA 24.985–25.405 ; dernier close 25.48)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 73% · **stop −4.39%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 44% (gap-down >1% 31% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.74% (p90 −2.24%) · haut méd +0.92% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −3.25%) · haut méd +1.24% · range méd 2.68%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.8%) · haut méd +1.4% · range méd 3.48%
- Excursion ouverture 60min (n=160) : bas méd −1.65% (p90 −4.36%) · haut méd +1.57% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.48 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (126/159) · gap 39% · délai 0.0min · rebond 59% (73/126) (MFE +1.32%)
   - −1.0% : fill 30min 57% · séance 71% (114/159) · gap 31% · délai 0.0min · rebond 59% (64/114) (MFE +1.23%)
   - −1.5% : fill 30min 46% · séance 64% (98/159) · gap 24% · délai 0.5min · rebond 62% (58/98) (MFE +1.42%)
   - −2.0% : fill 30min 42% · séance 55% (88/159) · gap 20% · délai 1.1min · rebond 64% (54/88) (MFE +1.59%)
   - −3.0% : fill 30min 27% · séance 49% (71/159) · gap 14% · délai 18.8min · rebond 59% (42/71) (MFE +1.6%)
   - −4.0% : fill 30min 20% · séance 38% (52/159) · gap 10% · délai 16.1min · rebond 67% (32/52) (MFE +1.63%)
   - −5.0% : fill 30min 17% · séance 32% (43/159) · gap 6% · délai 19.2min · rebond 73% (29/43) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.52%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.07%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.19%) → stop au-delà de −2.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=838 jambes) : jambe baissière méd −1.19% (p90 −2.86%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 94% (67/69) · rebond 48% (35/67)
      · −2.0% : fill 88% (60/69) · rebond 59% (33/60)
      · −3.0% : fill 82% (53/69) · rebond 56% (30/53)
      · −4.0% : fill 69% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 57% (35/69) · rebond 71% (23/35)
   - **flat** (15 séances) :
      · −1.0% : fill 94% (13/15) · rebond 87% (10/13)
      · −2.0% : fill 43% (8/15) · rebond 76% (5/8)
      · −3.0% : fill 10% (2/15) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/15) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/15) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 49% (34/75) · rebond 71% (19/34)
      · −2.0% : fill 28% (20/75) · rebond 74% (16/20)
      · −3.0% : fill 26% (16/75) · rebond 65% (10/16)
      · −4.0% : fill 17% (9/75) · rebond 65% (5/9)
      · −5.0% : fill 15% (8/75) · rebond 81% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (74 cas) · 23% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 76% si début vert vs 12% si rouge (base 44% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **76%** · continue >prix actuel 49% ; creux résiduel méd -1.61% (q20 -2.8%) → **SL/trailing à −2.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.61% / q75 +3.11% → **scale +1.61% / runner +3.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **12%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.11% .. +4.68%] · haut q95 +5.59% · bas q05 -4.37%
   - 60min (n=160) : retour [-4.21% .. +5.1%] · haut q95 +6.29% · bas q05 -5.46%
   - 2h (n=160) : retour [-4.78% .. +6.65%] · haut q95 +7.25% · bas q05 -5.82%
   - 4h (n=160) : retour [-5.64% .. +7.42%] · haut q95 +8.3% · bas q05 -6.95%
   - 6h (n=160) : retour [-6.47% .. +6.99%] · haut q95 +8.8% · bas q05 -8.11%
   - session (n=160) : retour [-7.26% .. +7.86%] · haut q95 +9.23% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.9  _(momentum haussier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist 0.266  _(bullish_recent)_
- **BB** : %B 0.79 · largeur 33.5%
- **ATR** : 1.92 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.209  _(distribution)_
- **Vol ratio** : 3.48  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.9  _(transition)_
- **MA** : MA20 27.81 · MA50 32.84 · MA200 33.7  _(prix > MA20)_
- **Dist MA** : MA20 +9.9% · MA50 -6.9% · MA200 -9.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90772 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
