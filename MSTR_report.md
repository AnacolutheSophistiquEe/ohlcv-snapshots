# MSTR

**Generated** : 2026-07-16T21:59:18.325362+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $94.03  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot $94.03 (+7.7% vs entrée) · entrée $87.31 · stop $84.26 · T1 $93.40 · R/R 2.0  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.009 _(réel 5 s)_ (GBM -0.24) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $86.09–$88.53 (mid $87.31)
- Spot actuel : $94.03 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : $84.26 (stop swing_plan-based (-10.39%))
- Targets : T1 $93.40 · R/R 2.0 | T2 $99.50 · R/R 4.0 | T3 $105.59 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $84.26


## Edge, scénarios & sizing

- EV/risk : -0.24 | EV/share : $-0.731 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 12.2 | bear 77.6 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.25% → cible +3.122% / stop −8.0%, p_fill 39%, n_eff≈16.1) : P(cible|rempli) **19%** · **EV/risk -0.037** (×p_fill ; si rempli -0.75% du capital)
  - **swing** (entrée dip −7.15% → cible +6.98% / stop −3.49%, p_fill 37%, n_eff≈15.6) : P(cible|rempli) **31%** · **EV/risk -0.009** (×p_fill ; si rempli -0.09% du capital)
  - **deep** (entrée dip −11.05% → cible +9.871% / stop −4.936%, p_fill 37%, n_eff≈13.2) : P(cible|rempli) **16%** · **EV/risk -0.207** (×p_fill ; si rempli -2.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→74% · +2.0%→57% · +3.0%→36% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.48% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.83%
- Profil de vol intra : ouverture 3.436% vs midi 1.278% vs clôture 1.313% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.623% ; recovery-V 39%
- **σ réalisé intraday** 4.199% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 63% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 98.6781 (VA 97.4519–98.9506 ; dernier close 97.42)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 68% · **stop −5.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 53% (gap-down >1% 38% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.02% (p90 −2.14%) · haut méd +0.68% · range méd 1.85%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −2.95%) · haut méd +1.09% · range méd 2.54%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.49%) · haut méd +1.36% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.38%) · haut méd +1.57% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (127/159) · gap 46% · délai 0.0min · rebond 52% (63/127) (MFE +1.41%)
   - −1.0% : fill 30min 63% · séance 75% (120/159) · gap 38% · délai 0.0min · rebond 56% (67/120) (MFE +1.36%)
   - −1.5% : fill 30min 56% · séance 68% (111/159) · gap 30% · délai 0.0min · rebond 54% (65/111) (MFE +1.32%)
   - −2.0% : fill 30min 47% · séance 62% (100/159) · gap 26% · délai 0.2min · rebond 57% (64/100) (MFE +1.22%)
   - −3.0% : fill 30min 35% · séance 52% (77/159) · gap 17% · délai 2.3min · rebond 56% (46/77) (MFE +1.52%)
   - −4.0% : fill 30min 24% · séance 43% (63/159) · gap 7% · délai 17.7min · rebond 58% (37/63) (MFE +1.51%)
   - −5.0% : fill 30min 18% · séance 32% (47/159) · gap 5% · délai 24.8min · rebond 68% (33/47) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.31%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.23% (p90 −2.83%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.3% (p90 −3.0%) → stop au-delà de −2.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=963 jambes) : jambe baissière méd −1.21% (p90 −2.82%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 46% (35/72)
      · −2.0% : fill 90% (65/73) · rebond 52% (38/65)
      · −3.0% : fill 82% (56/73) · rebond 56% (33/56)
      · −4.0% : fill 69% (47/73) · rebond 61% (30/47)
      · −5.0% : fill 54% (37/73) · rebond 70% (27/37)
   - **flat** (19 séances) :
      · −1.0% : fill 90% (18/19) · rebond 85% (12/18)
      · −2.0% : fill 60% (14/19) · rebond 66% (10/14)
      · −3.0% : fill 46% (10/19) · rebond 56% (6/10)
      · −4.0% : fill 29% (7/19) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/19) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 42% (30/67) · rebond 66% (20/30)
      · −2.0% : fill 29% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 19% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 17% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 51% si les 15 1res min sont vertes (75 cas) · 37% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 70% si début vert vs 16% si rouge (base 44% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **70%** · continue >prix actuel 56% ; creux résiduel méd -1.83% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.85% / q75 +3.0% → **scale +1.85% / runner +3.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **16%** (continue à baisser 64%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.61%** (au-delà de la MAE q10 -5.61%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +4.04%] · haut q95 +5.25% · bas q05 -4.17%
   - 60min (n=160) : retour [-4.94% .. +4.15%] · haut q95 +5.47% · bas q05 -5.31%
   - 2h (n=160) : retour [-4.74% .. +5.65%] · haut q95 +6.57% · bas q05 -5.34%
   - 4h (n=160) : retour [-7.33% .. +8.07%] · haut q95 +9.12% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.81% .. +6.93%] · haut q95 +9.93% · bas q05 -8.32%
   - session (n=160) : retour [-5.89% .. +6.29%] · haut q95 +9.93% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 58.3  _(momentum haussier)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 2.182  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 35.5%
- **ATR** : 7.39 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.243  _(distribution)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 57.0  _(transition)_
- **MA** : MA20 96.98 · MA50 131.4 · MA200 170.79  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -28.4% · MA200 -44.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87474 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
