# MSTR

**Generated** : 2026-08-18T21:58:21.430531+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $92.52  

> 🟡 **WAIT-FOR-DIP** — spot +0.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $92.52 (+0.8% vs entrée) · entrée $91.79 · stop $88.12 · T1 $93.70 · R/R 0.52  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM -0.036) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 995 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $91.41–$92.17 (mid $91.79)
- Spot actuel : $92.52 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $88.12 (stop swing_plan-based (-7.18%))
- Targets : T1 $93.70 · R/R 0.52 | T2 $95.60 · R/R 1.04 | T3 $97.50 · R/R 1.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $88.12


## Edge, scénarios & sizing

- EV/risk : -0.036 | EV/share : $-0.131 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 22 % | T3 14 %
- Kelly (position) : f* 0.087 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.4 | bear 10.7 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.781% → cible +2.073% / stop −4.0%, p_fill 83%, n_eff≈36.2) : P(cible|rempli) **51%** · **EV/risk +0.009** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −1.726% → cible +4.636% / stop −5.549%, p_fill 70%, n_eff≈30.1) : P(cible|rempli) **43%** · **EV/risk -0.160** (×p_fill ; si rempli -1.26% du capital)
  - **deep** (entrée dip −2.67% → cible +6.556% / stop −8.405%, p_fill 80%, n_eff≈33.3) : P(cible|rempli) **64%** · **EV/risk +0.144** (×p_fill ; si rempli +1.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→57% · +3.0%→40% · +5.0%→14% · +8.0%→6%
- Range intraday médian 5.38% (p90 9.51%) · excursion haute méd. +2.46% / basse méd. −2.55%
- Profil de vol intra : ouverture 3.362% vs midi 1.196% vs clôture 1.326% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr 0.016)_ ; drift intra méd. -0.197% ; recovery-V 28%
- **σ réalisé intraday** 3.612% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 66% / whipsaw 45%
- POC intraday (dernière séance, temps-au-prix) : 93.3275 (VA 92.2225–93.9225 ; dernier close 93.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 76% · **stop −4.8%** sous le fill (sous le bruit) · cible +1.98% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. -0.29% · baisse 53% (gap-down >1% 39% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −1.93%) · haut méd +0.75% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −2.52%) · haut méd +1.16% · range méd 2.38%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.28%) · haut méd +1.42% · range méd 3.12%
- Excursion ouverture 60min (n=160) : bas méd −1.6% (p90 −3.91%) · haut méd +1.8% · range méd 3.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (127/159) · gap 46% · délai 0.0min · rebond 51% (63/127) (MFE +1.25%)
   - −1.0% : fill 30min 62% · séance 74% (121/159) · gap 39% · délai 0.0min · rebond 56% (69/121) (MFE +1.11%)
   - −1.5% : fill 30min 54% · séance 68% (112/159) · gap 32% · délai 0.0min · rebond 58% (65/112) (MFE +1.44%)
   - −2.0% : fill 30min 48% · séance 61% (101/159) · gap 27% · délai 0.0min · rebond 61% (64/101) (MFE +1.32%)
   - −3.0% : fill 30min 34% · séance 48% (79/159) · gap 15% · délai 1.2min · rebond 58% (48/79) (MFE +1.56%)
   - −4.0% : fill 30min 23% · séance 39% (65/159) · gap 5% · délai 15.0min · rebond 66% (41/65) (MFE +1.66%)
   - −5.0% : fill 30min 15% · séance 28% (48/159) · gap 4% · délai 25.7min · rebond 76% (35/48) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.99% (p90 −2.72%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.06% (p90 −2.58%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=962 jambes) : jambe baissière méd −1.14% (p90 −2.81%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (77/78) · rebond 51% (39/77)
      · −2.0% : fill 91% (70/78) · rebond 59% (41/70)
      · −3.0% : fill 79% (62/78) · rebond 58% (37/62)
      · −4.0% : fill 65% (51/78) · rebond 69% (34/51)
      · −5.0% : fill 48% (39/78) · rebond 78% (29/39)
   - **flat** (18 séances) :
      · −1.0% : fill 79% (16/18) · rebond 73% (11/16)
      · −2.0% : fill 60% (12/18) · rebond 60% (8/12)
      · −3.0% : fill 26% (6/18) · rebond 57% (4/6)
      · −4.0% : fill 17% (5/18) · rebond 13% (2/5)
      · −5.0% : fill 13% (4/18) · rebond 16% (2/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 39% (28/63) · rebond 62% (19/28)
      · −2.0% : fill 21% (19/63) · rebond 72% (15/19)
      · −3.0% : fill 14% (11/63) · rebond 56% (7/11)
      · −4.0% : fill 13% (9/63) · rebond 66% (5/9)
      · −5.0% : fill 6% (5/63) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 54% si les 15 1res min sont vertes (80 cas) · 38% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 78% si début vert vs 15% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 42% ; creux résiduel méd -1.57% (q20 -3.41%) → **SL/trailing à −3.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.46% → **scale +1.59% / runner +2.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.88%** (au-delà de la MAE q10 -4.88%), cible rebond +1.64% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.41% .. +3.68%] · haut q95 +3.99% · bas q05 -3.95%
   - 60min (n=160) : retour [-4.73% .. +3.54%] · haut q95 +4.72% · bas q05 -5.25%
   - 2h (n=160) : retour [-4.49% .. +4.43%] · haut q95 +5.76% · bas q05 -5.29%
   - 4h (n=160) : retour [-5.74% .. +6.22%] · haut q95 +8.2% · bas q05 -7.04%
   - 6h (n=160) : retour [-5.91% .. +5.35%] · haut q95 +8.2% · bas q05 -7.75%
   - session (n=160) : retour [-5.3% .. +5.58%] · haut q95 +8.2% · bas q05 -7.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 49.0  _(neutre)_
- **ADX** : 9.6  _(pas de tendance nette)_
- **MACD** : hist 0.417  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 10.4%
- **ATR** : 5.05 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.011  _(neutre)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 96.04 · MA50 100.25 · MA200 146.22  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -7.7% · MA200 -36.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87521 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
