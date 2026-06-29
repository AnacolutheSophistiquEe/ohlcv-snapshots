# HOOD

**Generated** : 2026-06-29T00:21:08.367450+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $98.69  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $98.69 (+0.4% vs entrée) · entrée $98.26 · stop $95.31 · T1 $101.06 · R/R 0.95  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.079 _(réel 5 s)_ (GBM 0.011) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $97.83–$98.69 (mid $98.26)
- Spot actuel : $98.69 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $95.31 (stop swing_plan-based (-4.08%))
- Targets : T1 $101.06 · R/R 0.95 | T2 $103.87 · R/R 1.9 | T3 $106.67 · R/R 2.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $95.31


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.033 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 67.4 | bear 15.8 | side 16.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 395.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.433% → cible +2.854% / stop −3.0%, p_fill 86%, n_eff≈37.3) : P(cible|rempli) **35%** · **EV/risk -0.079** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −0.919% → cible +6.382% / stop −3.191%, p_fill 88%, n_eff≈36.2) : P(cible|rempli) **30%** · **EV/risk -0.137** (×p_fill ; si rempli -0.50% du capital)
  - **deep** (entrée dip −1.338% → cible +9.025% / stop −4.513%, p_fill 88%, n_eff≈35.2) : P(cible|rempli) **48%** · **EV/risk +0.427** (×p_fill ; si rempli +2.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→51% · +3.0%→35% · +5.0%→16% · +8.0%→5%
- Range intraday médian 4.89% (p90 8.55%) · excursion haute méd. +2.05% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.333% vs midi 1.065% vs clôture 1.026% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑1%/↓0% ; spike-down 63% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; momentum — autocorr 0.048)_ ; drift intra méd. 0.614% ; recovery-V 38%
- **σ réalisé intraday** 3.686% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 40% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 97.0828 (VA 95.8868–97.2322 ; dernier close 98.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 85% · **stop −4.8%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 54% (gap-down >1% 33% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.97%) · haut méd +0.82% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.03%) · haut méd +1.03% · range méd 2.59%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.82%) · haut méd +1.3% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −3.88%) · haut méd +1.6% · range méd 3.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 98.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (121/159) · gap 41% · délai 0.0min · rebond 53% (61/121) (MFE +1.36%)
   - −1.0% : fill 30min 57% · séance 65% (106/159) · gap 33% · délai 0.0min · rebond 56% (59/106) (MFE +1.26%)
   - −1.5% : fill 30min 51% · séance 62% (99/159) · gap 24% · délai 0.1min · rebond 51% (53/99) (MFE +1.12%)
   - −2.0% : fill 30min 44% · séance 57% (90/159) · gap 18% · délai 0.6min · rebond 61% (53/90) (MFE +1.28%)
   - −3.0% : fill 30min 33% · séance 44% (69/159) · gap 9% · délai 10.7min · rebond 66% (44/69) (MFE +1.7%)
   - −4.0% : fill 30min 21% · séance 34% (52/159) · gap 4% · délai 12.3min · rebond 74% (33/52) (MFE +1.99%)
   - −5.0% : fill 30min 13% · séance 22% (34/159) · gap 2% · délai 21.5min · rebond 85% (27/34) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.61%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.43%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.46%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=754 jambes) : jambe baissière méd −1.15% (p90 −2.72%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 95% (67/71) · rebond 52% (35/67)
      · −2.0% : fill 85% (58/71) · rebond 57% (33/58)
      · −3.0% : fill 71% (47/71) · rebond 61% (29/47)
      · −4.0% : fill 58% (38/71) · rebond 79% (27/38)
      · −5.0% : fill 42% (28/71) · rebond 84% (23/28)
   - **flat** (21 séances) :
      · −1.0% : fill 61% (15/21) · rebond 64% (10/15)
      · −2.0% : fill 55% (11/21) · rebond 48% (6/11)
      · −3.0% : fill 24% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 22% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 11% (3/21) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (24/67) · rebond 63% (14/24)
      · −2.0% : fill 29% (21/67) · rebond 82% (14/21)
      · −3.0% : fill 23% (16/67) · rebond 93% (13/16)
      · −4.0% : fill 13% (9/67) · rebond 80% (5/9)
      · −5.0% : fill 4% (3/67) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 72% si les 15 1res min sont vertes (70 cas) · 37% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 90% si début vert vs 17% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **90%** · continue >prix actuel 57% ; creux résiduel méd -1.26% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.01% / q75 +3.13% → **scale +1.01% / runner +3.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 60%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.51% .. +3.9%] · haut q95 +4.37% · bas q05 -4.59%
   - 60min (n=160) : retour [-3.65% .. +4.93%] · haut q95 +5.16% · bas q05 -4.87%
   - 2h (n=160) : retour [-4.16% .. +5.16%] · haut q95 +7.56% · bas q05 -5.58%
   - 4h (n=160) : retour [-4.66% .. +6.08%] · haut q95 +8.64% · bas q05 -6.16%
   - 6h (n=160) : retour [-5.66% .. +6.72%] · haut q95 +8.64% · bas q05 -6.88%
   - session (n=160) : retour [-5.03% .. +6.28%] · haut q95 +8.64% · bas q05 -7.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **42%**. Lecture précoce 30 min : signature présente → 21% vs absente 5% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.42% / p90 2.29%) · ~3.81 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **84%** (reprise méd 20.0 min, n=49)
   - −1.0% → **67%** (reprise méd 30.0 min, n=22)
   - −1.5% → **32%** (reprise méd 35.94 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.29%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.1% (q75 +9.8% / q95 +13.38%), MFE méd +7.16% / q90 +15.08%
   - Échelle scale-out : +7.16% (33%) / +12.41% (33%) / +15.08% (34%)
- **DÉSARMER** : repli > **−2.29%** depuis le plus-haut = décay → P(retournement) **71%** (préavis méd 134.36 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.08% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 75% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist -0.021  _(bearish_recent)_
- **BB** : %B 0.66 · largeur 33.7%
- **ATR** : 7.31 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.114  _(accumulation)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 42.2  _(transition)_
- **MA** : MA20 93.7 · MA50 85.22 · MA200 102.58  _(prix > MA20)_
- **Dist MA** : MA20 +5.3% · MA50 +15.8% · MA200 -3.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93787 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
