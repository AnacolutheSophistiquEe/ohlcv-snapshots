# PLTR

**Generated** : 2026-08-18T00:24:18.169744+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $172.55  

> 🟡 **WAIT-FOR-DIP** — spot +4.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $172.55 (+4.0% vs entrée) · entrée $165.85 · stop $153.72 · T1 $190.10 · R/R 2.0  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk 0.09 _(réel 5 s)_ (GBM 0.061) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 78.4 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $163.02–$168.68 (mid $165.85)
- Spot actuel : $172.55 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : $153.72 (stop swing_plan-based (-10.91%))
- Targets : T1 $190.10 · R/R 2.0 | T2 $207.52 · R/R 3.44 | T3 $208.16 · R/R 3.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $153.72


## Edge, scénarios & sizing

- EV/risk : 0.061 | EV/share : $0.739 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 66.6 | side 28.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 518.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.761% → cible +3.097% / stop −1.577%, p_fill 50%, n_eff≈20.5) : P(cible|rempli) **15%** · **EV/risk -0.037** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −3.882% → cible +14.623% / stop −7.312%, p_fill 34%, n_eff≈16.3) : P(cible|rempli) **15%** · **EV/risk +0.090** (×p_fill ; si rempli +1.92% du capital)
  - **deep** (entrée dip −6.0% → cible +27.947% / stop −13.734%, p_fill 41%, n_eff≈16.8) : P(cible|rempli) **38%** · **EV/risk +0.290** (×p_fill ; si rempli +9.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→50% · +3.0%→28% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.88% (p90 7.17%) · excursion haute méd. +2.0% / basse méd. −1.67%
- Profil de vol intra : ouverture 3.059% vs midi 0.739% vs clôture 0.832% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 23% · trend ↑2%/↓0% ; spike-down 54% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.0)_ ; drift intra méd. 0.704% ; recovery-V 28%
- **σ réalisé intraday** 2.768% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 48% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 176.8635 (VA 176.0985–178.6995 ; dernier close 174.02)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 51% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.02% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.16% · baisse 57% (gap-down >1% 28% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.09%) · haut méd +0.96% · range méd 1.94%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.84%) · haut méd +1.17% · range méd 2.4%
- Excursion ouverture 30min (n=160) : bas méd −1.11% (p90 −3.5%) · haut méd +1.24% · range méd 2.84%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.83%) · haut méd +1.42% · range méd 3.09%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.02 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 74% (118/159) · gap 39% · délai 0.0min · rebond 54% (65/118) (MFE +1.07%)
   - −1.0% : fill 30min 55% · séance 65% (108/159) · gap 28% · délai 0.0min · rebond 60% (64/108) (MFE +1.27%)
   - −1.5% : fill 30min 45% · séance 57% (93/159) · gap 22% · délai 0.6min · rebond 67% (61/93) (MFE +1.25%)
   - −2.0% : fill 30min 39% · séance 51% (80/159) · gap 13% · délai 1.8min · rebond 64% (50/80) (MFE +1.43%)
   - −3.0% : fill 30min 23% · séance 33% (56/159) · gap 8% · délai 5.2min · rebond 56% (27/56) (MFE +1.43%)
   - −4.0% : fill 30min 15% · séance 21% (39/159) · gap 5% · délai 11.6min · rebond 56% (20/39) (MFE +1.02%)
   - −5.0% : fill 30min 9% · séance 16% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −2.02%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −1.95%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.37%) → stop au-delà de −1.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=560 jambes) : jambe baissière méd −1.04% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 90% (69/73) · rebond 64% (42/69)
      · −2.0% : fill 76% (58/73) · rebond 67% (38/58)
      · −3.0% : fill 54% (41/73) · rebond 54% (20/41)
      · −4.0% : fill 36% (30/73) · rebond 51% (14/30)
      · −5.0% : fill 30% (23/73) · rebond 58% (12/23)
   - **flat** (28 séances) :
      · −1.0% : fill 83% (23/28) · rebond 37% (11/23)
      · −2.0% : fill 67% (14/28) · rebond 53% (8/14)
      · −3.0% : fill 36% (10/28) · rebond 57% (5/10)
      · −4.0% : fill 23% (7/28) · rebond 84% (5/7)
      · −5.0% : fill 12% (3/28) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 26% (16/58) · rebond 74% (11/16)
      · −2.0% : fill 14% (8/58) · rebond 70% (4/8)
      · −3.0% : fill 6% (5/58) · rebond 69% (2/5)
      · −4.0% : fill 1% (2/58) · rebond 25% (1/2)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 72% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 86% si début vert vs 21% si rouge (base 54% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **86%** · continue >prix actuel 59% ; creux résiduel méd -0.98% (q20 -1.77%) → **SL/trailing à −1.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.6% / q75 +2.52% → **scale +1.6% / runner +2.52%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **21%** (continue à baisser 48%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.28%** (au-delà de la MAE q10 -3.28%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.82% .. +3.87%] · haut q95 +4.52% · bas q05 -4.1%
   - 60min (n=160) : retour [-3.71% .. +4.82%] · haut q95 +5.32% · bas q05 -4.45%
   - 2h (n=160) : retour [-3.96% .. +5.81%] · haut q95 +6.7% · bas q05 -4.62%
   - 4h (n=160) : retour [-4.35% .. +5.74%] · haut q95 +6.74% · bas q05 -5.6%
   - 6h (n=160) : retour [-4.92% .. +6.44%] · haut q95 +7.34% · bas q05 -6.02%
   - session (n=160) : retour [-4.64% .. +6.65%] · haut q95 +7.46% · bas q05 -6.02%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 2.5% / strong 3.7%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 20% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.11% / p90 1.47%) · ~3.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 30.0 min, n=33)
   - −1.0% → **51%** (reprise méd 64.44 min, n=9)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.47%** (p90, défaut prudent ; serré/agressif −1.11%) ; extension open→close méd +6.19% (q75 +7.89% / q95 +12.13%), MFE méd +7.32% / q90 +13.49%
   - Échelle scale-out : +7.32% (33%) / +9.14% (33%) / +13.49% (34%)
- **DÉSARMER** : repli > **−1.47%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.49% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 62% du temps (retour médian dernière heure +0.21%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 78.4  _(surachat)_
- **ADX** : 29.4  _(tendance etablie)_
- **MACD** : hist 3.182  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 63.8%
- **ATR** : 8.91 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.163  _(accumulation)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 27.4  _(marche directionnel)_
- **MA** : MA20 147.42 · MA50 135.6 · MA200 152.01  _(prix > MA20)_
- **Dist MA** : MA20 +17.0% · MA50 +27.2% · MA200 +13.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91254 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
