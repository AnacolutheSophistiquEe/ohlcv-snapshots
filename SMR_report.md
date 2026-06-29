# SMR

**Generated** : 2026-06-29T21:57:18.809878+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.26  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $10.26 (+1.5% vs entrée) · entrée $10.11 · stop $9.65 · T1 $11.03 · R/R 2.0  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.125 _(réel 5 s)_ (GBM 0.08) · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.52% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $10.04–$10.19 (mid $10.11)
- Spot actuel : $10.26 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $9.65 (stop swing_plan-based (-12.53%))
- Targets : T1 $11.03 · R/R 2.0 | T2 $11.14 · R/R 2.24 | T3 $11.25 · R/R 2.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.65


## Edge, scénarios & sizing

- EV/risk : 0.08 | EV/share : $0.036 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.235 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.8 | bear 53.6 | side 27.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.447% → cible +9.036% / stop −4.519%, p_fill 60%, n_eff≈28.0) : P(cible|rempli) **5%** · **EV/risk -0.125** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −3.186% → cible +19.302% / stop −9.652%, p_fill 62%, n_eff≈27.1) : P(cible|rempli) **10%** · **EV/risk -0.073** (×p_fill ; si rempli -1.13% du capital)
  - **deep** (entrée dip −4.929% → cible +30.148% / stop −15.074%, p_fill 64%, n_eff≈26.1) : P(cible|rempli) **8%** · **EV/risk -0.045** (×p_fill ; si rempli -1.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→54% · +5.0%→36% · +8.0%→19%
- Range intraday médian 7.23% (p90 12.61%) · excursion haute méd. +3.11% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.817% vs midi 1.543% vs clôture 1.843% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.55% ; recovery-V 25%
- **σ réalisé intraday** 5.351% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 40% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 9.9898 (VA 9.9087–10.0708 ; dernier close 10.085)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 57% · rebond 75% · **stop −6.0%** sous le fill (sous le bruit) · cible +3.4% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 63% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.37% (p90 −3.6%) · haut méd +1.11% · range méd 2.91%
- Excursion ouverture 15min (n=160) : bas méd −1.75% (p90 −3.98%) · haut méd +1.38% · range méd 3.87%
- Excursion ouverture 30min (n=160) : bas méd −2.07% (p90 −5.6%) · haut méd +1.94% · range méd 4.44%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −6.18%) · haut méd +2.59% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.085 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 78% · séance 82% (132/159) · gap 55% · délai 0.0min · rebond 64% (81/132) (MFE +1.77%)
   - −1.0% : fill 30min 72% · séance 78% (126/159) · gap 45% · délai 0.0min · rebond 66% (83/126) (MFE +2.01%)
   - −1.5% : fill 30min 69% · séance 75% (120/159) · gap 41% · délai 0.0min · rebond 73% (86/120) (MFE +2.22%)
   - −2.0% : fill 30min 64% · séance 70% (114/159) · gap 30% · délai 0.0min · rebond 69% (83/114) (MFE +2.54%)
   - −3.0% : fill 30min 54% · séance 64% (103/159) · gap 14% · délai 1.9min · rebond 77% (84/103) (MFE +3.11%)
   - −4.0% : fill 30min 42% · séance 57% (87/159) · gap 7% · délai 6.8min · rebond 75% (67/87) (MFE +3.4%)
   - −5.0% : fill 30min 27% · séance 42% (64/159) · gap 4% · délai 14.5min · rebond 71% (47/64) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.97%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.73%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −3.85%) → stop au-delà de −2.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1205 jambes) : jambe baissière méd −1.39% (p90 −3.16%) · ~15.0 jambes/séance
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
      · −1.0% : fill 47% (33/63) · rebond 56% (22/33)
      · −2.0% : fill 40% (27/63) · rebond 58% (19/27)
      · −3.0% : fill 33% (21/63) · rebond 76% (17/21)
      · −4.0% : fill 29% (16/63) · rebond 67% (11/16)
      · −5.0% : fill 21% (14/63) · rebond 44% (8/14)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 66% si les 15 1res min sont vertes (63 cas) · 37% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 79% si début vert vs 17% si rouge (base 50% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **79%** · continue >prix actuel 43% ; creux résiduel méd -2.53% (q20 -3.94%) → **SL/trailing à −3.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.56% / q75 +4.98% → **scale +2.56% / runner +4.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.39%** (au-delà de la MAE q10 -7.39%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.85% .. +4.54%] · haut q95 +6.62% · bas q05 -6.89%
   - 60min (n=160) : retour [-6.56% .. +6.02%] · haut q95 +8.9% · bas q05 -8.04%
   - 2h (n=160) : retour [-8.07% .. +9.93%] · haut q95 +11.46% · bas q05 -9.54%
   - 4h (n=160) : retour [-9.01% .. +8.43%] · haut q95 +11.47% · bas q05 -11.02%
   - 6h (n=160) : retour [-8.7% .. +8.76%] · haut q95 +11.68% · bas q05 -11.09%
   - session (n=160) : retour [-8.77% .. +10.97%] · haut q95 +11.74% · bas q05 -11.11%


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 11.8  _(pas de tendance nette)_
- **MACD** : hist -0.014  _(bearish_recent)_
- **BB** : %B 0.38 · largeur 44.1%
- **ATR** : 0.96 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.113  _(distribution)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 60.5  _(transition)_
- **MA** : MA20 10.82 · MA50 11.57 · MA200 19.96  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -11.3% · MA200 -48.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90863 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
