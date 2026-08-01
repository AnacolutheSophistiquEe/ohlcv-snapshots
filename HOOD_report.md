# HOOD

**Generated** : 2026-08-01T21:53:33.860116+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $86.56  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $86.56 (+1.4% vs entrée) · entrée $85.39 · stop $81.12 · T1 $87.16 · R/R 0.41  
> ↳ P(T1 av. stop) 62 % _(réel 5 s)_ · EV/risk 0.012 _(réel 5 s)_ (GBM 0.007) · ¼-Kelly 0.041 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

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
- Stop : $81.12 (stop swing_plan-based (-10.27%))
- Targets : T1 $87.16 · R/R 0.41 | T2 $88.94 · R/R 0.83 | T3 $90.72 · R/R 1.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $81.12


## Edge, scénarios & sizing

- EV/risk : 0.007 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 27 % | T3 21 %
- Kelly (position) : f* 0.164 | ¼-Kelly 0.041 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.2 | bear 12.5 | side 80.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.358% → cible +2.081% / stop −5.0%, p_fill 76%, n_eff≈29.7) : P(cible|rempli) **62%** · **EV/risk +0.012** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −2.98% → cible +4.653% / stop −7.514%, p_fill 58%, n_eff≈22.0) : P(cible|rempli) **52%** · **EV/risk -0.059** (×p_fill ; si rempli -0.77% du capital)
  - **deep** (entrée dip −4.605% → cible +6.58% / stop −11.463%, p_fill 51%, n_eff≈18.3) : P(cible|rempli) **54%** · **EV/risk -0.101** (×p_fill ; si rempli -2.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→80% · +2.0%→55% · +3.0%→35% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.11% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.648% vs midi 1.072% vs clôture 1.088% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.006)_ ; drift intra méd. -0.209% ; recovery-V 30%
- **σ réalisé intraday** 3.794% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 51% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 89.6054 (VA 89.1464–90.8676 ; dernier close 89.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 79% · **stop −4.69%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 55% (gap-down >1% 37% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.52%) · haut méd +0.85% · range méd 2.15%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.84%) · haut méd +1.2% · range méd 2.9%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.95%) · haut méd +1.44% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.47%) · haut méd +1.66% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 89.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (124/159) · gap 46% · délai 0.0min · rebond 55% (62/124) (MFE +1.37%)
   - −1.0% : fill 30min 62% · séance 70% (110/159) · gap 37% · délai 0.0min · rebond 60% (64/110) (MFE +1.39%)
   - −1.5% : fill 30min 52% · séance 64% (101/159) · gap 25% · délai 0.0min · rebond 56% (56/101) (MFE +1.37%)
   - −2.0% : fill 30min 45% · séance 55% (89/159) · gap 17% · délai 0.2min · rebond 64% (54/89) (MFE +1.35%)
   - −3.0% : fill 30min 33% · séance 43% (67/159) · gap 9% · délai 6.6min · rebond 74% (46/67) (MFE +1.9%)
   - −4.0% : fill 30min 20% · séance 35% (52/159) · gap 4% · délai 12.0min · rebond 79% (35/52) (MFE +2.33%)
   - −5.0% : fill 30min 13% · séance 22% (33/159) · gap 3% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.7%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.49%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.56%) → stop au-delà de −1.76% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=748 jambes) : jambe baissière méd −1.15% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 97% (71/74) · rebond 54% (37/71)
      · −2.0% : fill 82% (60/74) · rebond 60% (35/60)
      · −3.0% : fill 70% (49/74) · rebond 71% (33/49)
      · −4.0% : fill 60% (40/74) · rebond 81% (29/40)
      · −5.0% : fill 39% (27/74) · rebond 72% (20/27)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 40% (23/64) · rebond 70% (16/23)
      · −2.0% : fill 23% (17/64) · rebond 86% (12/17)
      · −3.0% : fill 18% (12/64) · rebond 97% (11/12)
      · −4.0% : fill 12% (7/64) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/64) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 61% si les 15 1res min sont vertes (72 cas) · 36% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 72% si début vert vs 26% si rouge (base 47% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **72%** · continue >prix actuel 51% ; creux résiduel méd -1.78% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.4% → **scale +1.62% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **26%** (continue à baisser 54%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +2.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.57% .. +4.15%] · haut q95 +4.73% · bas q05 -5.17%
   - 60min (n=160) : retour [-3.68% .. +4.39%] · haut q95 +6.17% · bas q05 -5.52%
   - 2h (n=160) : retour [-4.71% .. +5.37%] · haut q95 +6.99% · bas q05 -6.06%
   - 4h (n=160) : retour [-4.88% .. +5.74%] · haut q95 +8.29% · bas q05 -6.82%
   - 6h (n=160) : retour [-5.75% .. +6.67%] · haut q95 +8.29% · bas q05 -7.18%
   - session (n=160) : retour [-5.43% .. +6.14%] · haut q95 +8.41% · bas q05 -7.56%


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88969 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
