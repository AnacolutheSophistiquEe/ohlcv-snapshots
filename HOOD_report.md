# HOOD

**Generated** : 2026-08-02T15:06:10.045418+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $86.56  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $86.56 (+1.4% vs entrée) · entrée $85.39 · stop $82.83 · T1 $87.16 · R/R 0.69  
> ↳ P(T1 av. stop) 60 % _(réel 5 s)_ · EV/risk 0.079 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -43 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $85.03–$85.74 (mid $85.39)
- Spot actuel : $86.56 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $82.83 (stop swing_plan-based (-10.27%))
- Targets : T1 $87.16 · R/R 0.69 | T2 $88.94 · R/R 1.39 | T3 $90.72 · R/R 2.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $82.83


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : $0.036 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 27 % | T3 21 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.2 | bear 12.5 | side 80.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.351% → cible +2.081% / stop −3.0%, p_fill 78%, n_eff≈30.1) : P(cible|rempli) **60%** · **EV/risk +0.079** (×p_fill ; si rempli +0.30% du capital)
  - **swing** (entrée dip −2.98% → cible +4.653% / stop −7.514%, p_fill 62%, n_eff≈22.6) : P(cible|rempli) **44%** · **EV/risk -0.145** (×p_fill ; si rempli -1.76% du capital)
  - **deep** (entrée dip −4.605% → cible +6.58% / stop −11.463%, p_fill 47%, n_eff≈18.2) : P(cible|rempli) **54%** · **EV/risk -0.092** (×p_fill ; si rempli -2.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→56% · +3.0%→36% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.17% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.704% vs midi 1.074% vs clôture 1.128% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑1%/↓0% ; spike-down 70% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr 0.004)_ ; drift intra méd. -0.387% ; recovery-V 33%
- **σ réalisé intraday** 3.881% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 51% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 87.238 (VA 85.51–88.534 ; dernier close 86.57)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 34% · rebond 79% · **stop −4.69%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.16% · baisse 55% (gap-down >1% 36% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.71%) · haut méd +0.95% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.93%) · haut méd +1.26% · range méd 2.93%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −4.36%) · haut méd +1.67% · range méd 3.51%
- Excursion ouverture 60min (n=160) : bas méd −2.11% (p90 −4.7%) · haut méd +1.71% · range méd 3.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 86.57 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 81% (126/159) · gap 44% · délai 0.0min · rebond 57% (64/126) (MFE +1.37%)
   - −1.0% : fill 30min 64% · séance 72% (112/159) · gap 36% · délai 0.0min · rebond 62% (66/112) (MFE +1.51%)
   - −1.5% : fill 30min 54% · séance 65% (103/159) · gap 24% · délai 0.2min · rebond 59% (58/103) (MFE +1.74%)
   - −2.0% : fill 30min 45% · séance 56% (91/159) · gap 16% · délai 0.5min · rebond 66% (56/91) (MFE +1.46%)
   - −3.0% : fill 30min 34% · séance 45% (69/159) · gap 9% · délai 6.6min · rebond 76% (48/69) (MFE +2.1%)
   - −4.0% : fill 30min 20% · séance 34% (52/159) · gap 4% · délai 12.0min · rebond 79% (35/52) (MFE +2.33%)
   - −5.0% : fill 30min 13% · séance 22% (33/159) · gap 3% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.64%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.47%) → stop au-delà de −1.78% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.54%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=748 jambes) : jambe baissière méd −1.14% (p90 −2.87%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 97% (72/75) · rebond 55% (38/72)
      · −2.0% : fill 83% (61/75) · rebond 62% (36/61)
      · −3.0% : fill 71% (50/75) · rebond 73% (34/50)
      · −4.0% : fill 57% (40/75) · rebond 81% (29/40)
      · −5.0% : fill 38% (27/75) · rebond 72% (20/27)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (63 séances) :
      · −1.0% : fill 42% (24/63) · rebond 73% (17/24)
      · −2.0% : fill 26% (18/63) · rebond 88% (13/18)
      · −3.0% : fill 22% (13/63) · rebond 98% (12/13)
      · −4.0% : fill 11% (7/63) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/63) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 63% si les 15 1res min sont vertes (71 cas) · 34% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 72% si début vert vs 27% si rouge (base 47% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 51% ; creux résiduel méd -1.78% (q20 -3.3%) → **SL/trailing à −3.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.41% → **scale +1.62% / runner +3.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **27%** (continue à baisser 54%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +2.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.56% .. +4.13%] · haut q95 +4.65% · bas q05 -5.26%
   - 60min (n=160) : retour [-3.68% .. +4.36%] · haut q95 +5.98% · bas q05 -5.58%
   - 2h (n=160) : retour [-4.78% .. +5.11%] · haut q95 +6.7% · bas q05 -6.03%
   - 4h (n=160) : retour [-4.82% .. +5.71%] · haut q95 +8.26% · bas q05 -6.78%
   - 6h (n=160) : retour [-5.75% .. +6.6%] · haut q95 +8.26% · bas q05 -7.15%
   - session (n=160) : retour [-5.4% .. +6.1%] · haut q95 +8.29% · bas q05 -7.55%


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
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 26.8  _(survente)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist -2.955  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 38.9%
- **ATR** : 6.31 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.145  _(distribution)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 37.4  _(marche directionnel)_
- **MA** : MA20 103.7 · MA50 96.64 · MA200 99.29  _(prix < MA20)_
- **Dist MA** : MA20 -16.5% · MA50 -10.4% · MA200 -12.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88920 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
