# 000660

**Generated** : 2026-07-21T21:38:57.325812+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩1836000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1836000.00 (+2.0% vs entrée) · entrée ₩1799429.36 · stop ₩1724665.08 · T1 ₩1855000.00 · R/R 0.74  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.124 _(réel 5 s)_ (GBM -0.019) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.15% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1788315.23–₩1810543.49 (mid ₩1799429.36)
- Spot actuel : ₩1836000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1724665.08 (stop swing_plan-based (-11.58%))
- Targets : T1 ₩1855000.00 · R/R 0.74 | T2 ₩2019833.22 · R/R 2.95 | T3 ₩2044006.91 · R/R 3.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1724665.08


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : ₩-1457.224 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.086 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.1 | bear 62.3 | side 8.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.988% → cible +3.088% / stop −4.155%, p_fill 71%, n_eff≈26.8) : P(cible|rempli) **35%** · **EV/risk -0.124** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −4.383% → cible +15.055% / stop −7.527%, p_fill 64%, n_eff≈21.3) : P(cible|rempli) **22%** · **EV/risk -0.197** (×p_fill ; si rempli -2.34% du capital)
  - **deep** (entrée dip −6.768% → cible +40.624% / stop −18.0%, p_fill 55%, n_eff≈16.7) : P(cible|rempli) **4%** · **EV/risk -0.324** (×p_fill ; si rempli -10.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→81% · +2.0%→57% · +3.0%→39% · +5.0%→25% · +8.0%→14%
- Range intraday médian 6.15% (p90 11.16%) · excursion haute méd. +2.33% / basse méd. −2.5%
- Profil de vol intra : ouverture 3.012% vs midi 1.211% vs clôture 1.506% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑2%/↓0% ; spike-down 66% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.596% ; recovery-V 26%
- **σ réalisé intraday** 5.146% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 69% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 1776950.0 (VA 1761350.0–1804250.0 ; dernier close 1775000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 48% · rebond 79% · **stop −8.68%** sous le fill (sous le bruit) · cible +2.69% · R/R 0.31 (high win-rate)
- Gaps overnight (n=139) : méd. -0.14% · baisse 52% (gap-down >1% 38% · >2% 30%)
- Excursion ouverture 5min (n=140) : bas méd −0.57% (p90 −1.61%) · haut méd +0.99% · range méd 1.51%
- Excursion ouverture 15min (n=140) : bas méd −0.77% (p90 −2.14%) · haut méd +1.18% · range méd 2.05%
- Excursion ouverture 30min (n=140) : bas méd −1.28% (p90 −3.03%) · haut méd +1.36% · range méd 2.75%
- Excursion ouverture 60min (n=140) : bas méd −1.34% (p90 −3.79%) · haut méd +1.7% · range méd 3.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1775000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 67% (87/139) · gap 43% · délai 0.0min · rebond 56% (46/87) (MFE +1.64%)
   - −1.0% : fill 30min 55% · séance 64% (80/139) · gap 38% · délai 0.0min · rebond 66% (50/80) (MFE +1.85%)
   - −1.5% : fill 30min 50% · séance 58% (71/139) · gap 35% · délai 0.0min · rebond 67% (45/71) (MFE +1.84%)
   - −2.0% : fill 30min 42% · séance 52% (64/139) · gap 30% · délai 0.0min · rebond 65% (42/64) (MFE +1.89%)
   - −3.0% : fill 30min 41% · séance 48% (56/139) · gap 24% · délai 0.0min · rebond 79% (42/56) (MFE +2.69%)
   - −4.0% : fill 30min 29% · séance 40% (43/139) · gap 14% · délai 3.5min · rebond 77% (33/43) (MFE +2.78%)
   - −5.0% : fill 30min 15% · séance 32% (34/139) · gap 11% · délai 30.4min · rebond 74% (26/34) (MFE +2.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −2.56%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −3.42%) → stop au-delà de −2.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.68%) → stop au-delà de −1.86% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=713 jambes) : jambe baissière méd −1.32% (p90 −3.34%) · ~12.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (59/61) · rebond 55% (32/59)
      · −2.0% : fill 87% (50/61) · rebond 62% (30/50)
      · −3.0% : fill 82% (45/61) · rebond 76% (32/45)
      · −4.0% : fill 72% (38/61) · rebond 73% (28/38)
      · −5.0% : fill 60% (31/61) · rebond 71% (23/31)
   - **flat** (11 séances) :
      · −1.0% : fill 88% (8/11) · rebond 81% (6/8)
      · −2.0% : fill 70% (6/11) · rebond 80% (5/6)
      · −3.0% : fill 60% (5/11) · rebond 100% (5/5)
      · −4.0% : fill 31% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 14% (1/11) · rebond 100% (1/1)
   - **gap-up** (67 séances) :
      · −1.0% : fill 26% (13/67) · rebond 98% (12/13)
      · −2.0% : fill 14% (8/67) · rebond 75% (7/8)
      · −3.0% : fill 12% (6/67) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/67) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 46% en base · 55% si les 15 1res min sont vertes (76 cas) · 34% si rouges (64 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 74% si début vert vs 17% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **74%** · continue >prix actuel 48% ; creux résiduel méd -1.69% (q20 -6.12%) → **SL/trailing à −6.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +3.33% → **scale +1.35% / runner +3.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=64) : edge inversé — récupère vert seulement **17%** (continue à baisser 63%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.75%** (au-delà de la MAE q10 -6.75%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-2.83% .. +3.56%] · haut q95 +4.28% · bas q05 -3.67%
   - 60min (n=140) : retour [-3.52% .. +5.72%] · haut q95 +6.76% · bas q05 -5.14%
   - 2h (n=140) : retour [-4.6% .. +5.63%] · haut q95 +8.34% · bas q05 -6.47%
   - 4h (n=140) : retour [-5.76% .. +7.11%] · haut q95 +8.52% · bas q05 -8.1%
   - 6h (n=140) : retour [-7.17% .. +7.79%] · haut q95 +9.75% · bas q05 -8.99%
   - session (n=140) : retour [-6.48% .. +8.1%] · haut q95 +9.75% · bas q05 -8.99%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 0% / strong 6.4%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.9  _(momentum baissier)_
- **ADX** : 28.4  _(tendance etablie)_
- **MACD** : hist -77555.835  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 59.9%
- **ATR** : 249214.29 (95.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.221  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 45.7  _(transition)_
- **MA** : MA20 2274200.0 · MA50 2196977.5 · MA200 1122168.69  _(prix < MA20)_
- **Dist MA** : MA20 -19.3% · MA50 -16.4% · MA200 +63.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88154 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
