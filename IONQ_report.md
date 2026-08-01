# IONQ

**Generated** : 2026-08-01T21:47:52.510751+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $36.44  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $36.44 (+1.4% vs entrée) · entrée $35.95 · stop $34.48 · T1 $38.88 · R/R 1.99  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.197 _(réel 5 s)_ (GBM -0.039) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.08% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $35.74–$36.15 (mid $35.95)
- Spot actuel : $36.44 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $34.48 (stop swing_plan-based (-11.94%))
- Targets : T1 $38.88 · R/R 1.99 | T2 $38.94 · R/R 2.03 | T3 $39.00 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $34.48


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : $-0.058 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 30 % | T3 30 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.5 | bear 37.3 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.345% → cible +8.161% / stop −4.08%, p_fill 77%, n_eff≈32.4) : P(cible|rempli) **6%** · **EV/risk -0.197** (×p_fill ; si rempli -1.04% du capital)
  - **swing** (entrée dip −2.965% → cible +18.498% / stop −9.249%, p_fill 74%, n_eff≈29.7) : P(cible|rempli) **5%** · **EV/risk -0.380** (×p_fill ; si rempli -4.77% du capital)
  - **deep** (entrée dip −4.578% → cible +8.96% / stop −11.163%, p_fill 87%, n_eff≈32.3) : P(cible|rempli) **28%** · **EV/risk -0.381** (×p_fill ; si rempli -4.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→65% · +3.0%→61% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.68% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −3.27%
- Profil de vol intra : ouverture 5.21% vs midi 1.572% vs clôture 1.683% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; momentum — autocorr 0.032)_ ; drift intra méd. -1.237% ; recovery-V 28%
- **σ réalisé intraday** 4.734% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 32.6604 (VA 32.2869–33.2829 ; dernier close 32.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.4% · baisse 56% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.27% (p90 −2.93%) · haut méd +1.01% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −4.27%) · haut méd +1.33% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.92% (p90 −5.29%) · haut méd +1.66% · range méd 4.51%
- Excursion ouverture 60min (n=160) : bas méd −2.52% (p90 −5.96%) · haut méd +1.91% · range méd 5.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 83% (133/159) · gap 46% · délai 0.0min · rebond 67% (91/133) (MFE +1.87%)
   - −1.0% : fill 30min 72% · séance 80% (127/159) · gap 39% · délai 0.0min · rebond 73% (93/127) (MFE +2.35%)
   - −1.5% : fill 30min 69% · séance 78% (122/159) · gap 32% · délai 0.0min · rebond 66% (83/122) (MFE +2.51%)
   - −2.0% : fill 30min 60% · séance 70% (112/159) · gap 20% · délai 0.3min · rebond 66% (76/112) (MFE +2.53%)
   - −3.0% : fill 30min 49% · séance 61% (93/159) · gap 10% · délai 7.7min · rebond 72% (67/93) (MFE +2.8%)
   - −4.0% : fill 30min 31% · séance 47% (74/159) · gap 6% · délai 16.7min · rebond 72% (55/74) (MFE +2.19%)
   - −5.0% : fill 30min 20% · séance 41% (64/159) · gap 2% · délai 31.1min · rebond 83% (55/64) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.89%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.04% (p90 −3.63%) → stop au-delà de −2.55% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.99%) → stop au-delà de −2.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1122 jambes) : jambe baissière méd −1.34% (p90 −3.31%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 73% (56/75)
      · −2.0% : fill 95% (71/75) · rebond 71% (53/71)
      · −3.0% : fill 83% (61/75) · rebond 70% (45/61)
      · −4.0% : fill 63% (46/75) · rebond 69% (34/46)
      · −5.0% : fill 56% (40/75) · rebond 77% (32/40)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 56% (39/68) · rebond 71% (28/39)
      · −2.0% : fill 40% (29/68) · rebond 52% (17/29)
      · −3.0% : fill 34% (23/68) · rebond 78% (17/23)
      · −4.0% : fill 27% (20/68) · rebond 79% (17/20)
      · −5.0% : fill 24% (17/68) · rebond 100% (17/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 51% si les 15 1res min sont vertes (79 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 76% si début vert vs 17% si rouge (base 42% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -2.29% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +2.8% → **scale +1.84% / runner +2.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **17%** (continue à baisser 56%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.29%** (au-delà de la MAE q10 -4.29%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +6.73%] · haut q95 +7.84% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.19% .. +5.41%] · haut q95 +8.36% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.42% .. +7.84%] · haut q95 +8.92% · bas q05 -7.33%
   - 4h (n=160) : retour [-7.26% .. +7.13%] · haut q95 +10.14% · bas q05 -8.33%
   - 6h (n=160) : retour [-7.51% .. +7.47%] · haut q95 +10.14% · bas q05 -8.61%
   - session (n=160) : retour [-7.36% .. +8.1%] · haut q95 +10.14% · bas q05 -8.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.89% / p90 2.79%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=39)
   - −1.0% → **74%** (reprise méd 20.0 min, n=24)
   - −1.5% → **59%** (reprise méd 38.13 min, n=12)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.79%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +7.79% (q75 +10.75% / q95 +18.2%), MFE méd +9.27% / q90 +19.18%
   - Échelle scale-out : +9.27% (33%) / +12.82% (33%) / +19.18% (34%)
- **DÉSARMER** : repli > **−2.79%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +19.18% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 44.2  _(momentum baissier)_
- **ADX** : 39.2  _(tendance etablie)_
- **MACD** : hist 0.499  _(bullish_recent)_
- **BB** : %B 0.43 · largeur 51.5%
- **ATR** : 2.59 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.323  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 37.89 · MA50 50.66 · MA200 46.3  _(prix < MA20)_
- **Dist MA** : MA20 -3.8% · MA50 -28.1% · MA200 -21.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88679 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
