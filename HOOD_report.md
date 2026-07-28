# HOOD

**Generated** : 2026-07-28T00:28:35.658157+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $95.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $95.65 (+3.7% vs entrée) · entrée $92.20 · stop $89.44 · T1 $97.58 · R/R 1.95  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.03 _(réel 5 s)_ (GBM 0.097) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $91.75–$92.66 (mid $92.20)
- Spot actuel : $95.65 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $89.44 (stop swing_plan-based (-10.46%))
- Targets : T1 $97.58 · R/R 1.95 | T2 $98.30 · R/R 2.21 | T3 $99.02 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.44


## Edge, scénarios & sizing

- EV/risk : 0.097 | EV/share : $0.267 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.064 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.8 | bear 11.7 | side 59.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.598% → cible +5.832% / stop −3.0%, p_fill 33%, n_eff≈12.3) : P(cible|rempli) **14%** · **EV/risk -0.030** (×p_fill ; si rempli -0.28% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→55% · +3.0%→35% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.05% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.62% vs midi 1.063% vs clôture 1.067% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 67% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.033% ; recovery-V 30%
- **σ réalisé intraday** 3.784% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 49% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 95.2535 (VA 94.4485–95.7365 ; dernier close 94.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 33% · rebond 76% · **stop −4.83%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 54% (gap-down >1% 37% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.37%) · haut méd +1.01% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.11% (p90 −3.62%) · haut méd +1.19% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.86%) · haut méd +1.47% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −3.91%) · haut méd +1.7% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (122/159) · gap 45% · délai 0.0min · rebond 54% (61/122) (MFE +1.38%)
   - −1.0% : fill 30min 62% · séance 69% (108/159) · gap 37% · délai 0.0min · rebond 59% (62/108) (MFE +1.31%)
   - −1.5% : fill 30min 51% · séance 62% (99/159) · gap 25% · délai 0.0min · rebond 55% (54/99) (MFE +1.22%)
   - −2.0% : fill 30min 43% · séance 54% (88/159) · gap 16% · délai 0.3min · rebond 65% (53/88) (MFE +1.34%)
   - −3.0% : fill 30min 33% · séance 42% (66/159) · gap 8% · délai 6.7min · rebond 71% (44/66) (MFE +1.89%)
   - −4.0% : fill 30min 20% · séance 33% (50/159) · gap 4% · délai 12.0min · rebond 76% (33/50) (MFE +2.33%)
   - −5.0% : fill 30min 12% · séance 22% (32/159) · gap 3% · délai 21.3min · rebond 74% (24/32) (MFE +2.34%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −2.57%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.5%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.56%) → stop au-delà de −1.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=754 jambes) : jambe baissière méd −1.14% (p90 −2.8%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 97% (69/72) · rebond 54% (36/69)
      · −2.0% : fill 80% (58/72) · rebond 61% (34/58)
      · −3.0% : fill 68% (47/72) · rebond 68% (31/47)
      · −4.0% : fill 56% (38/72) · rebond 79% (27/38)
      · −5.0% : fill 38% (26/72) · rebond 69% (19/26)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 37% (23/66) · rebond 66% (15/23)
      · −2.0% : fill 24% (18/66) · rebond 84% (12/18)
      · −3.0% : fill 19% (13/66) · rebond 95% (11/13)
      · −4.0% : fill 12% (7/66) · rebond 88% (5/7)
      · −5.0% : fill 7% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (72 cas) · 34% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 72% si début vert vs 25% si rouge (base 48% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 50% ; creux résiduel méd -1.8% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.4% → **scale +1.62% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **25%** (continue à baisser 53%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.12%** (au-delà de la MAE q10 -4.12%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.55% .. +4.27%] · haut q95 +4.86% · bas q05 -5.21%
   - 60min (n=160) : retour [-3.82% .. +4.52%] · haut q95 +6.2% · bas q05 -5.67%
   - 2h (n=160) : retour [-4.81% .. +5.75%] · haut q95 +7.4% · bas q05 -6.09%
   - 4h (n=160) : retour [-4.96% .. +5.98%] · haut q95 +8.32% · bas q05 -6.87%
   - 6h (n=160) : retour [-5.75% .. +6.71%] · haut q95 +8.33% · bas q05 -7.22%
   - session (n=160) : retour [-5.52% .. +6.24%] · haut q95 +8.58% · bas q05 -7.59%


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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.9  _(survente)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist -2.311  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 25.0%
- **ATR** : 6.4 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.015  _(neutre)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 46.6  _(transition)_
- **MA** : MA20 107.27 · MA50 95.34 · MA200 100.68  _(prix < MA20)_
- **Dist MA** : MA20 -10.8% · MA50 +0.3% · MA200 -5.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88395 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
