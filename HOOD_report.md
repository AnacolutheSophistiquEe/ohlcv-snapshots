# HOOD

**Generated** : 2026-08-11T00:31:38.612314+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $94.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $94.52 (+3.3% vs entrée) · entrée $91.47 · stop $88.73 · T1 $93.45 · R/R 0.72  
> ↳ P(T1 av. stop) 60 % _(réel 5 s)_ · EV/risk 0.076 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $91.08–$91.87 (mid $91.47)
- Spot actuel : $94.52 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : $88.73 (stop swing_plan-based (-12.6%))
- Targets : T1 $93.45 · R/R 0.72 | T2 $95.43 · R/R 1.45 | T3 $97.40 · R/R 2.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $88.73


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 23 % | T3 20 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.1 | bear 56.7 | side 33.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.227% → cible +2.162% / stop −3.0%, p_fill 34%, n_eff≈14.5) : P(cible|rempli) **60%** · **EV/risk +0.076** (×p_fill ; si rempli +0.69% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→56% · +3.0%→35% · +5.0%→20% · +8.0%→6%
- Range intraday médian 5.08% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.671% vs midi 1.041% vs clôture 1.129% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; neutre — autocorr 0.014)_ ; drift intra méd. -0.149% ; recovery-V 38%
- **σ réalisé intraday** 3.733% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 49% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 93.2848 (VA 92.7212–94.1702 ; dernier close 93.28)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 31% · rebond 79% · **stop −4.7%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 51% (gap-down >1% 34% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −2.67%) · haut méd +1.03% · range méd 2.1%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.84%) · haut méd +1.37% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.52% (p90 −4.09%) · haut méd +1.76% · range méd 3.5%
- Excursion ouverture 60min (n=160) : bas méd −1.87% (p90 −4.64%) · haut méd +1.79% · range méd 3.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.28 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (124/159) · gap 42% · délai 0.0min · rebond 57% (65/124) (MFE +1.39%)
   - −1.0% : fill 30min 63% · séance 70% (110/159) · gap 34% · délai 0.0min · rebond 62% (64/110) (MFE +1.54%)
   - −1.5% : fill 30min 51% · séance 61% (101/159) · gap 24% · délai 0.0min · rebond 60% (57/101) (MFE +1.6%)
   - −2.0% : fill 30min 43% · séance 53% (90/159) · gap 17% · délai 0.4min · rebond 68% (56/90) (MFE +1.53%)
   - −3.0% : fill 30min 31% · séance 41% (68/159) · gap 8% · délai 6.6min · rebond 76% (47/68) (MFE +2.11%)
   - −4.0% : fill 30min 18% · séance 31% (51/159) · gap 4% · délai 11.9min · rebond 79% (34/51) (MFE +2.33%)
   - −5.0% : fill 30min 12% · séance 20% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.56%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.43%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.44%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=753 jambes) : jambe baissière méd −1.14% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 53% (36/70)
      · −2.0% : fill 84% (61/73) · rebond 63% (36/61)
      · −3.0% : fill 69% (49/73) · rebond 73% (33/49)
      · −4.0% : fill 55% (39/73) · rebond 81% (28/39)
      · −5.0% : fill 36% (27/73) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 74% (15/20) · rebond 80% (10/15)
      · −2.0% : fill 46% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 16% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 15% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 7% (3/20) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 41% (25/66) · rebond 76% (18/25)
      · −2.0% : fill 23% (18/66) · rebond 88% (13/18)
      · −3.0% : fill 19% (13/66) · rebond 98% (12/13)
      · −4.0% : fill 10% (7/66) · rebond 88% (5/7)
      · −5.0% : fill 6% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (76 cas) · 34% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 69% si début vert vs 29% si rouge (base 48% · écart 39 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **69%** · continue >prix actuel 47% ; creux résiduel méd -1.56% (q20 -3.19%) → **SL/trailing à −3.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.22% → **scale +1.62% / runner +3.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **29%** (continue à baisser 52%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.07%** (au-delà de la MAE q10 -4.07%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.54% .. +4.07%] · haut q95 +4.49% · bas q05 -5.25%
   - 60min (n=160) : retour [-3.66% .. +4.36%] · haut q95 +5.17% · bas q05 -5.46%
   - 2h (n=160) : retour [-4.67% .. +4.87%] · haut q95 +6.57% · bas q05 -5.94%
   - 4h (n=160) : retour [-4.69% .. +5.77%] · haut q95 +7.97% · bas q05 -6.56%
   - 6h (n=160) : retour [-5.74% .. +6.42%] · haut q95 +7.97% · bas q05 -7.1%
   - session (n=160) : retour [-5.31% .. +6.08%] · haut q95 +7.97% · bas q05 -7.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 16% vs absente 3% (base 8%)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.0  _(momentum baissier)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist -0.464  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 33.9%
- **ATR** : 5.2 (35.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.154  _(distribution)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 43.4  _(transition)_
- **MA** : MA20 97.41 · MA50 98.53 · MA200 98.08  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -4.1% · MA200 -3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87635 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
