# HOOD

**Generated** : 2026-07-30T00:29:54.579420+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $89.84  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $89.84 (+2.3% vs entrée) · entrée $87.85 · stop $83.46 · T1 $89.96 · R/R 0.48  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk 0.034 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $87.42–$88.27 (mid $87.85)
- Spot actuel : $89.84 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $83.46 (stop swing_plan-based (-7.44%))
- Targets : T1 $89.96 · R/R 0.48 | T2 $92.08 · R/R 0.96 | T3 $94.20 · R/R 1.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $83.46


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 23 % | T3 21 %
- Kelly (position) : f* 0.114 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.3 | bear 25.8 | side 67.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.221% → cible +2.409% / stop −5.0%, p_fill 56%, n_eff≈20.5) : P(cible|rempli) **52%** · **EV/risk +0.034** (×p_fill ; si rempli +0.30% du capital)
  - **swing** (entrée dip −4.878% → cible +5.387% / stop −2.694%, p_fill 33%, n_eff≈12.1) : P(cible|rempli) **24%** · **EV/risk -0.110** (×p_fill ; si rempli -0.91% du capital)
  - **deep** (entrée dip −7.538% → cible +7.618% / stop −3.809%, p_fill 30%, n_eff≈10.5) : P(cible|rempli) **32%** · **EV/risk -0.049** (×p_fill ; si rempli -0.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→55% · +3.0%→35% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.12% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.671% vs midi 1.072% vs clôture 1.064% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.087% ; recovery-V 32%
- **σ réalisé intraday** 3.805% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 49% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 91.7972 (VA 91.7972–93.6107 ; dernier close 92.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 76% · **stop −4.16%** sous le fill (sous le bruit) · cible +2.82% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 54% (gap-down >1% 38% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.61%) · haut méd +0.89% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.11% (p90 −3.84%) · haut méd +1.18% · range méd 2.9%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.99%) · haut méd +1.47% · range méd 3.48%
- Excursion ouverture 60min (n=160) : bas méd −1.87% (p90 −4.53%) · haut méd +1.7% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 92.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (123/159) · gap 45% · délai 0.0min · rebond 54% (61/123) (MFE +1.38%)
   - −1.0% : fill 30min 61% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 59% (63/109) (MFE +1.32%)
   - −1.5% : fill 30min 52% · séance 63% (100/159) · gap 26% · délai 0.0min · rebond 55% (55/100) (MFE +1.23%)
   - −2.0% : fill 30min 44% · séance 54% (88/159) · gap 17% · délai 0.1min · rebond 63% (53/88) (MFE +1.31%)
   - −3.0% : fill 30min 33% · séance 42% (66/159) · gap 9% · délai 2.7min · rebond 72% (45/66) (MFE +1.79%)
   - −4.0% : fill 30min 21% · séance 34% (51/159) · gap 4% · délai 11.2min · rebond 78% (34/51) (MFE +2.22%)
   - −5.0% : fill 30min 14% · séance 23% (33/159) · gap 3% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.73%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.49%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.56%) → stop au-delà de −1.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=750 jambes) : jambe baissière méd −1.14% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 52% (36/70)
      · −2.0% : fill 81% (59/73) · rebond 58% (34/59)
      · −3.0% : fill 69% (48/73) · rebond 70% (32/48)
      · −4.0% : fill 58% (39/73) · rebond 80% (28/39)
      · −5.0% : fill 41% (27/73) · rebond 72% (20/27)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (65 séances) :
      · −1.0% : fill 39% (23/65) · rebond 70% (16/23)
      · −2.0% : fill 23% (17/65) · rebond 86% (12/17)
      · −3.0% : fill 18% (12/65) · rebond 97% (11/12)
      · −4.0% : fill 12% (7/65) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/65) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 61% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 72% si début vert vs 26% si rouge (base 48% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **72%** · continue >prix actuel 51% ; creux résiduel méd -1.79% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +3.4% → **scale +1.63% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **26%** (continue à baisser 52%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.58% .. +4.18%] · haut q95 +4.77% · bas q05 -5.19%
   - 60min (n=160) : retour [-3.7% .. +4.43%] · haut q95 +6.17% · bas q05 -5.57%
   - 2h (n=160) : retour [-4.75% .. +5.5%] · haut q95 +7.13% · bas q05 -6.07%
   - 4h (n=160) : retour [-4.91% .. +5.81%] · haut q95 +8.3% · bas q05 -6.83%
   - 6h (n=160) : retour [-5.75% .. +6.7%] · haut q95 +8.3% · bas q05 -7.19%
   - session (n=160) : retour [-5.45% .. +6.17%] · haut q95 +8.47% · bas q05 -7.57%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 20% vs absente 3% (base 8%)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 25.8  _(survente)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist -2.814  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 31.7%
- **ATR** : 6.54 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.085  _(distribution)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 40.8  _(transition)_
- **MA** : MA20 106.11 · MA50 96.2 · MA200 99.82  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -6.6% · MA200 -10.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88685 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
