# SMR

**Generated** : 2026-07-01T00:20:29.199233+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.03  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $10.03 (+0.9% vs entrée) · entrée $9.94 · stop $9.40 · T1 $11.03 · R/R 2.02  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM 0.027) · ¼-Kelly 0.057 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.46% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.86–$10.01 (mid $9.94)
- Spot actuel : $10.03 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $9.40 (stop swing_plan-based (-12.07%))
- Targets : T1 $11.03 · R/R 2.02 | T2 $11.04 · R/R 2.04 | T3 $11.05 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.40


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : $0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.228 | ¼-Kelly 0.057 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.4 | bear 54.0 | side 25.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.905% → cible +10.93% / stop −5.464%, p_fill 74%, n_eff≈31.5) : P(cible|rempli) **11%** · **EV/risk +0.009** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −2.008% → cible +20.559% / stop −10.279%, p_fill 73%, n_eff≈32.4) : P(cible|rempli) **7%** · **EV/risk -0.072** (×p_fill ; si rempli -1.02% du capital)
  - **deep** (entrée dip −3.088% → cible +30.611% / stop −15.305%, p_fill 78%, n_eff≈32.7) : P(cible|rempli) **6%** · **EV/risk -0.192** (×p_fill ; si rempli -3.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→52% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.11% (p90 12.61%) · excursion haute méd. +3.07% / basse méd. −3.09%
- Profil de vol intra : ouverture 4.821% vs midi 1.551% vs clôture 1.823% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.51% ; recovery-V 23%
- **σ réalisé intraday** 5.327% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 43% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 10.2395 (VA 10.0015–10.3075 ; dernier close 10.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 56% · rebond 75% · **stop −6.0%** sous le fill (sous le bruit) · cible +3.4% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 62% (gap-down >1% 44% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.33% (p90 −3.57%) · haut méd +1.12% · range méd 2.88%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.98%) · haut méd +1.43% · range méd 3.84%
- Excursion ouverture 30min (n=160) : bas méd −2.04% (p90 −5.59%) · haut méd +1.97% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −6.13%) · haut méd +2.56% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (132/159) · gap 54% · délai 0.0min · rebond 65% (81/132) (MFE +1.97%)
   - −1.0% : fill 30min 71% · séance 79% (126/159) · gap 44% · délai 0.0min · rebond 67% (83/126) (MFE +2.1%)
   - −1.5% : fill 30min 68% · séance 75% (120/159) · gap 40% · délai 0.0min · rebond 73% (86/120) (MFE +2.28%)
   - −2.0% : fill 30min 63% · séance 71% (115/159) · gap 30% · délai 0.1min · rebond 70% (84/115) (MFE +2.69%)
   - −3.0% : fill 30min 53% · séance 62% (103/159) · gap 14% · délai 1.9min · rebond 77% (84/103) (MFE +3.11%)
   - −4.0% : fill 30min 42% · séance 56% (87/159) · gap 7% · délai 6.8min · rebond 75% (67/87) (MFE +3.4%)
   - −5.0% : fill 30min 26% · séance 41% (64/159) · gap 4% · délai 14.5min · rebond 71% (47/64) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.96%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.77% (p90 −3.67%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −3.85%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1202 jambes) : jambe baissière méd −1.36% (p90 −3.16%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 71% (54/83)
      · −2.0% : fill 92% (79/83) · rebond 75% (59/79)
      · −3.0% : fill 86% (76/83) · rebond 81% (63/76)
      · −4.0% : fill 75% (65/83) · rebond 78% (53/65)
      · −5.0% : fill 57% (46/83) · rebond 80% (36/46)
   - **flat** (13 séances) :
      · −1.0% : fill 71% (10/13) · rebond 55% (7/10)
      · −2.0% : fill 55% (8/13) · rebond 43% (5/8)
      · −3.0% : fill 50% (6/13) · rebond 42% (4/6)
      · −4.0% : fill 50% (6/13) · rebond 57% (3/6)
      · −5.0% : fill 34% (4/13) · rebond 51% (3/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 50% (33/63) · rebond 60% (22/33)
      · −2.0% : fill 43% (28/63) · rebond 63% (20/28)
      · −3.0% : fill 31% (21/63) · rebond 76% (17/21)
      · −4.0% : fill 28% (16/63) · rebond 67% (11/16)
      · −5.0% : fill 20% (14/63) · rebond 44% (8/14)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 63% si les 15 1res min sont vertes (64 cas) · 37% si rouges (96 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 79% si début vert vs 16% si rouge (base 49% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -2.53% (q20 -3.94%) → **SL/trailing à −3.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.56% / q75 +4.98% → **scale +2.56% / runner +4.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **16%** (continue à baisser 54%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.27%** (au-delà de la MAE q10 -7.27%), cible rebond +2.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.79% .. +4.52%] · haut q95 +6.6% · bas q05 -6.87%
   - 60min (n=160) : retour [-6.52% .. +5.97%] · haut q95 +8.87% · bas q05 -8.0%
   - 2h (n=160) : retour [-8.05% .. +9.81%] · haut q95 +11.44% · bas q05 -9.49%
   - 4h (n=160) : retour [-8.97% .. +8.43%] · haut q95 +11.44% · bas q05 -10.98%
   - 6h (n=160) : retour [-8.69% .. +8.76%] · haut q95 +11.67% · bas q05 -11.08%
   - session (n=160) : retour [-8.71% .. +10.96%] · haut q95 +11.74% · bas q05 -11.1%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0.6% / strong 4.4%) · base = 8 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **12%**. Lecture précoce 30 min : signature présente → 12% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.19% (p75 1.56% / p90 2.99%) · ~5.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 15.0 min, n=44)
   - −1.0% → **81%** (reprise méd 19.98 min, n=26)
   - −1.5% → **72%** (reprise méd 40.32 min, n=11)
   - −2.0% → **89%** (reprise méd 49.41 min, n=8)
   - −3.0% → **100%** (reprise méd 84.35 min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.99%** (p90, défaut prudent ; serré/agressif −1.56%) ; extension open→close méd +11.04% (q75 +11.76% / q95 +11.9%), MFE méd +12.98% / q90 +13.48%
   - Échelle scale-out : +12.98% (33%) / +13.38% (33%) / +13.48% (34%)
- **DÉSARMER** : repli > **−2.99%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.48% : P(retournement après) 0% (mèche méd 2.37%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.2  _(neutre)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist -0.021  _(bearish_recent)_
- **BB** : %B 0.35 · largeur 41.2%
- **ATR** : 0.9 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 58.1  _(transition)_
- **MA** : MA20 10.68 · MA50 11.51 · MA200 19.84  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -12.9% · MA200 -49.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90962 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
